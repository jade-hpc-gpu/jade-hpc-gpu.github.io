---
title: Access
subtitle: Get access to JADE HPC facilities
layout: page
permalink: "/access/"
---


<hr />
<h2 id="simple">Introduction</h2>

As agreed with EPSRC, the use of JADE is to be split approximately 50:30:20 between Machine/Deep Learning (ML), Molecular Dynamics (MD), and other applications, with up to 10% of the use being for research in non-EPSRC areas.

JADE is particularly intended for applications using up to 8 GPUs with a very high performance NVlink interconnect.  It is not designed for MPI applications spanning multple compute nodes; for this purpose users should apply to use the GPU system which is part of the [Cambridge Peta-5 GPU system](http://hpc-sig.org.uk/wp-content/blogs.dir/sites/63/2017/02/2017_02_09_tier2_Peta-5.pdf).

#### Machine Learning ####

PIs in the partner universities should contact their [local RSE support](http://www.jade.ac.uk/support/) or <a href="mailto:wes.armour@oerc.ox.ac.uk">Prof Wes Armour</a>.

PIs from other universities should apply for time through the twice-yearly [EPSRC Tier 2 RAP (Resource Allocation Panel)](https://www.epsrc.ac.uk/files/funding/calls/2018/tier-2rapopenaccesscallspring2018/
).


#### Molecular Dynamics ####

 Time for Molecular Dynamics applications will only be allocated via the [BioSim HEC](http://www.hecbiosim.ac.uk/).


#### Other Applications of JADE ####


All UK academic users are eligible to apply for time for Other applications (not Machine Learning or Molecular Dynamics) through the twice-yearly [EPSRC Tier 2 RAP (Resource Allocation Panel)](https://www.epsrc.ac.uk/funding/calls/tier2openaccess/). Pump-priming time will also be available; please contact <a href="mailto:wes.armour@oerc.ox.ac.uk">Prof Wes Armour</a> in the first instance.

<hr />
<h2 id="simple">Academic Access</h2>

To obtaining a user account you need:

* a Hartree SAFE account;
* a JADE project account and
* a JADE project access code.

#### SAFE accounts ####

This is a web account which will show you which projects you belong to, and the accounts which you have in them.

Before applying for a SAFE account, you should have an SSH key-pair ready, so you are ready to provide your public key as part of the SAFE registration process.  Information on generating and using SSH keys is available [here](https://stfc.service-now.com/hartreecentre?id=kb_article&sys_id=9dbedf2edba96200e47b7cc9bf9619a2).  Contact 
your local University RSE Support for any help.

Once you have your public SSH key ready, apply for your SAFE account [here](https://um.hartree.stfc.ac.uk/hartree/login.jsp) and providing all of the required information.

Once your account is approved, you receive an email giving your initial password.  When you login for the first time you will be asked to change it to a new one.

Further details on the registration process are available [here](https://stfc.service-now.com/hartreecentre?id=kb_article&sys_id=9dbedf2edba96200e47b7cc9bf9619a2).


#### JADE accounts ####

Use your [SAFE account](https://um.hartree.stfc.ac.uk/hartree/) to apply for an account on JADE.  Select the appropriate project from the drop-down list, enter the JADE project access which you have from the project PI or manager, and then click "Request".


The approval process goes through several steps:

* approval by the PI or project manager (once this is done the SAFE status changes to Pending);
* initial account setup (once this is done the SAFE status changes to Active) and
* completion of account setup.

Once the account setup is complete, your SAFE account has full details on your new project account and you get a confirmation email.  This process should not take more than 2 working days.  If it takes more than that, check if the PI or project manager is aware that you have applied, and therefore your application needs their approval through the SAFE system.

Assuming your SAFE userid is **xyz**, and your project suffix is **abc**, then your project account username will be **xyz-abc** and you will login to JADE using the command

~~~ bash
ssh -l xyz-abc jade.hartree.stfc.ac.uk
~~~

Note that some users may belong to more than one project, in which case they will have different account usernames for each project, and all of them will be listed on their SAFE web account.

Each project account will have a separate file structure, and separate quotas for GPU time, filestore and other system resources.

Note also that JADE has multiple front-end systems, and because of this some SSH software operating under stringent security settings might give warnings about possible man-in-the-middle attacks because of apparent changes in machine settings.  This is a known issue and is being addressed, but in the meantime these warnings can be safely ignored.


#### ServiceNow Account ####

Additionally, an optional step is applying for a Hartree **ServiceNow** account, which is a web account used for reporting any operational issues with JADE.   An account can be obtained following [here](https://stfc.service-now.com/hartreecentre).

Note the guidance which explains that on first login, you will not have a password so you need to click on the link which says "reset your password here".

Due to a problem with synchronising userids between ServiceNow and JADE, it is possible that ServiceNow may say that your email address is not recognised.  If this happens, please send an email to <a href="mailto:hartree@stfc.ac.uk">hartree@stfc.ac.uk</a> and ask them to add you to the ServiceNow database.

<!--- Other sections to come
<hr />
<h2 id="simple">Simple Access Methods</h2>
<hr />
<h2 id="grant">Grant Access</h2>
<hr />
<h2 id="other">Other Access Routes</h2>
--->
