=======================================================================
Joint Academic Data Science Endeavour - running Jobs on the JADE system
=======================================================================
Last modified: 28/7/2017

The whole system from the user perspective is interacted with via the Slurm Workload Manager on the login nodes. Via this scheduler, access to the compute nodes, can be interactive or batch. The installed application software consists of a mixture of docker container images, supplied by Nvidia, and executables built from source. Both container images and executables can use the system either interactively or in batch mode.

It is only possible to ssh onto a node which has been allocated to the user. Once the session completes the ssh access is removed. Access to the global parallel file system is from the login nodes and all compute nodes. Any data on this file system is retained after a session on the nodes completes. There is also access to local disc space on each node. Access to this file system is only possible during a Slurm session. Once the session completes the local disc data is removed.

The software initially installed on the machine is listed in the following table:

.. csv-table:: 
   :header: Application,Version,Note
   :widths: 20, 20, 10

    GNU compiler suite,	4.8.4,	part of O/S
    PGI compiler suite,	17.4,	 
    OpenMPI,	1.10.2,	Supplied with PGI
    OpenMPI,	1.10.5a1,	Supplied with PGI
    Gromacs,	2016.3,	Supplied by Nvidia
    NAMD,	2.12,

This software has been built from source and installed as modules. To list the source built applications do:

::

    $ module avail
    ----------------------------------------------------- /jmain01/apps/modules -----------------------------
    gromacs/2016.3           openmpi/1.10.2/2017      pgi/17.4(default)        pgi64/17.4(default)     
    PrgEnv-pgi/17.4(default)      NAMD/2.12      openmpi/1.10.5a1/GNU     pgi/2017             pgi64/2017

The applications initially supplied by Nvidia as containers are listed in the following table:

.. csv-table:: 
   :header: Application,Version
   :widths: 20, 20

    Caffe,	17.04
    Theano,	17.04
    Torch,	17.04

To list the containers and version available on the system do:

::

    $ containers
    REPOSITORY                    TAG                 IMAGE ID                CREATED               SIZE
    nvidia/cuda                  latest              15e5dedd88c5        4 weeks ago          1.67 GB
    nvcr.io/nvidia/caffe         17.04               87c288427f2d        6 weeks ago          2.794 GB
    nvcr.io/nvidia/theano        17.04               24943feafc9b         8 weeks ago          2.386 GB
    nvcr.io/nvidia/torch         17.04               a337ffb42c8e         9 weeks ago          2.9 GB

The following brief notes explain how run the various applications.

Gromacs
#######

The latest version of the source was used. The following build instructions were followed: http://www.nvidia.com/object/gromacs-installation.html

The code was compiled using OpenMPI v1.10.5a1 and GCC v4.8.4 with the following command:

::

    CC=mpicc CXX=mpicxx cmake /jmain01/home/atostest/Building/gromacs-2016.3 
    -DGMX_OPENMP=ON 
    -DGMX_GPU=ON 
    -DGPU_DEPLOYMENT_KIT_ROOT_DIR=/usr/local/cuda-8.0/targets/x86_64-linux 
    -DCUDA_TOOLKIT_ROOT_DIR=/usr/local/cuda-8.0/targets/x86_64-linux 
    -DNVML_INCLUDE_DIR=/usr/local/cuda-8.0/targets/x86_64-linux/include 
    -DNVML_LIBRARY=/usr/lib/nvidia-375/libnvidia-ml.so 
    -DHWLOC_INCLUDE_DIRS=/usr/mpi/gcc/openmpi-1.10.5a1/include/openmpi/opal/mca/hwloc/hwloc191/hwloc/include 
    -DGMX_BUILD_OWN_FFTW=ON 
    -DGMX_PREFER_STATIC_LIBS=ON 
    -DCMAKE_BUILD_TYPE=Release 
    -DGMX_BUILD_UNITTESTS=ON 
    -DCMAKE_INSTALL_PREFIX=/jmain01/home/atostest/gromacs-2016.3

The following is an example Slurm script to run the code using one of the regression tests from the installation:

::

    #!/bin/bash
    #SBATCH --nodes=2
    #SBATCH --ntasks=4
    #SBATCH -p all
    #SBATCH -J Gromacs
    #SBATCH --time=01:00:00
    #SBATCH --gres=gpu:2
    module load gromacs/2016.3
    ./gmxtest.pl -np 8 -verbose simple

As can be seem the code will run across multiple compute nodes. Also, the number of GPUs per node is requested using the ``gres`` option. In this example the user will request 2 out of the possible 8 on the nodes.

There is access to the local disc space on each node whilst the batch session is in progress. It can be accessed via: ``/raid/local_scratch/$USERID``

Any data within the directory will be lost once the session completes.

NAMD
####

The latest version of the source code was used and built using OpenMPI v1.10.5a1 and GCC v4.8.4 following instructions from: http://www.nvidia.com/object/gpu-accelerated-applications-namd-installation.html

Charm++ was built using: 

::

    ./build charm++ verbs-linux-x86_64 gcc smp --with-production

NAMD was built using the following: 

::

    ./config Linux-x86_64-g++ --charm-arch verbs-linux-x86_64-smp-gcc --with-cuda --cuda-prefix /usr/local/cuda-8.0


For the decision on the number of threads to use per node, take a look at: http://www.nvidia.com/object/gpu-accelerated-applications-namd-running-jobs.html

::

    #!/bin/bash
    #SBATCH --nodes=2
    #SBATCH -p all
    #SBATCH -J NAMD
    #SBATCH --time=01:00:00
    #SBATCH --gres=gpu:8

    module load NAMD/2.12

    #set up the nodelist file
    srun hostname > hf-1
    sed 's/^/host /' hf-1 > hf && rm hf-1
    echo 'group main ++shell ssh' | cat - hf  > hf-1 && mv hf-1 hf

    $NAMDROOT/charmrun ++p 64 ++ppn 4 $NAMDROOT/namd2 
    ++nodelist hf +setcpuaffinity +pemap 0-19,20-39 +commap 0,20 
    +devices 3,1 src/alanin

    rm hf

As can be seen from the script setting above the code will run across multiple nodes, in this case 2 nodes.

Using Containerised Applications
################################

On entering the container the present working directory will be the user's home directory: ``/home_directory``

Any files you copy into ``/home_directory`` will have the same userid as normal and will be available once exiting the container. The local disk space on the node is available at: ``/local_scratch/$USERID``

This is 6.6TB in size but any data will be lost once the interactive session is ended. There are two ways of interacting with the containerised applications.

1.Interactive Mode
++++++++++++++++++

All the applications in containers can be launched interactively in the same way using 1 compute node at a time. The number of GPUs to be used per node is requested using the ``gres`` option. To request an interactive session on a compute node the following command is issued from the login node: 

::

    srun --gres=gpu:2 --pty /jmain01/apps/docker/caffe 17.04

This command will show the following, which is now running on a compute node:

::

    ================
    ==NVIDIA Caffe== 
    ================
    
    NVIDIA Release 17.04 (build 26740)
    
    Container image Copyright (c) 2017, NVIDIA CORPORATION.  All rights reserved.
    Copyright (c) 2014, 2015, The Regents of the University of California (Regents)
    All rights reserved.
    
    Various files include modifications (c) NVIDIA CORPORATION.  All rights reserved.
    NVIDIA modifications are covered by the license terms that apply to the underlying project or file.
    
    groups: cannot find name for group ID 1002
    I have no name!@124cf0e3582e:/home_directory$

Note. The warnings in the last two lines can be ignored. To exit the container, issue the "exit" command. To launch the other containers the commands are: 

::

    srun --gres=gpu:8 --pty /jmain01/apps/docker/theano 17.04
    srun --gres=gpu:4 --pty /jmain01/apps/docker/torch 17.04

2.Batch Mode
++++++++++++

There are wrappers for launching the containers in batch mode. For example, to launch the Torch application change directory to where the launching script is, in this case called ``submit-char.sh``: 

::

    cd /jmain01/home/atostest/char-rnn-master

A Slurm batch script is used to launch the code, such as:

::

    #!/bin/bash
    #SBATCH --nodes=1
    #SBATCH -p all
    #SBATCH -J Torch
    #SBATCH --gres=gpu:8
    #SBATCH --time=01:00:00

    /jmain01/apps/docker/torch-batch -c ./submit-char.sh

The output will appear in the slurm standard output file.

Each of the containerised applications has its own batch launching script:

::

    /jmain01/apps/docker/torch-batch
    /jmain01/apps/docker/caffe-batch
    /jmain01/apps/docker/theano-batch

More Information
################

JADE Web site: http://www.arc.ox.ac.uk/content/jade

Mike Giles' Web site: http://people.maths.ox.ac.uk/~gilesm/JADE/

STFC Web site: https://www.hartree.stfc.ac.uk/Pages/Hartree-Centre-welcomes-new-HPC-computing-facility-to-support-machine-learning.aspx

