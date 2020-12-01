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

To obtain a user account you need:

* a Hartree Centre Self Service Portal Account;
* a Hartree SAFE account;
* a JADE project account and
* a JADE project access code.

#### Hartree Centre Self Service Portal Account ####

In order to gain technical support for the JADE machine firstly register for access to the
Hartree Centre Self-Service Portal (HCSSP), which is a web account used for
reporting any operational issues with JADE and provides access to the Hartree knowledge base. An account can be obtained [here](https://stfc.service-now.com/hcssp), using the
register option in the top right hand corner. Once registered a user will be able to access
the user guides linked below.

To access the Hartree Centre status page click [here](https://stfc.service-now.com/hcssp?id=services_status).

For any account issues, please contact your local University JADE [point of contact](http://www.jade.ac.uk/support) in the first instance.

#### Accessing the JADE Machine - SAFE Accounts ####

SAFE is the user account management system that the Hartree Centre currently use for
accessing machines, this is a web account which will show you which projects you
belong to, and your accounts associated with them.

Before applying for a SAFE account it is necessary to prepare an SSH key-pair, this will
enable you to provide the public key as part of the SAFE registration. Information on
generating and using SSH keys is available [here](https://stfc.service-now.com/kb?id=kb_article_view&amp;sys_kb_id=318854b7db451410b40c9334ca9619ec) for users who have already registered for the Hartree Self Service Portal.

* Contact your local University JADE [point of contact](http://www.jade.ac.uk/support) for technical SSH key help.
* Contact [hartree@stfc.ac.uk](mailto:hartree@stfc.ac.uk) if you are unable to access the links provided.

Once your public SSH key is ready, apply for a SAFE account [here](https://um.hartree.stfc.ac.uk/hartree/login.jsp). An email will be
sent to your inbox containing a temporary password. Upon first login it will be necessary
to update your password.

Further details on the SAFE registration process are available [here](https://stfc.service-now.com/kb?id=kb_article_view&amp;sys_kb_id=3eae9073db851410b40c9334ca961991).

In order to request access to a project, contact the PI of the project for the access code.
Request access and await approval by the PI of the project. In order to learn how to
request access, please read the section below.


#### JADE accounts ####

Use your [SAFE account](https://um.hartree.stfc.ac.uk/hartree/) to apply for an account on JADE.  Select the appropriate project from the drop-down list, found beneath your personal information and any existing login accounts. Then enter the JADE project access code which you will have received from the project PI or manager, and then click "Request".


The approval process goes through several steps:

* approval by the PI or project manager (once this is done the SAFE status changes to Pending);
* initial account setup (once this is done the SAFE status changes to Active) and
* completion of account setup. Please note, that account setup is a manual process, and any changes/updates to your SSH key will be manually uploaded by the Hartree Centre support team.

Once the account setup is complete, your SAFE account has full details on your new project account and you get a confirmation email.  This process should not take more than 2 working days.  If it takes more than that, check if the PI or project manager is aware that you have applied, and therefore your application needs their approval through the SAFE system.

Assuming your SAFE userid is **xyz**, and your project suffix is **abc**, then your project account username will be **xyz-abc** and you will login to JADE using the command

~~~ bash
ssh -l xyz-abc jade.hartree.stfc.ac.uk
~~~

Note that some users may belong to more than one project, in which case they will have different account usernames for each project, and all of them will be listed on their SAFE web account.

Each project account will have a separate file structure, and separate quotas for GPU time, filestore and other system resources.

Note also that JADE has multiple front-end systems, and because of this some SSH software operating under stringent security settings might give warnings about possible man-in-the-middle attacks because of apparent changes in machine settings.  This is a known issue and is being addressed, but in the meantime these warnings can be safely ignored.

<!--- Other sections to come
<hr />
<h2 id="simple">Simple Access Methods</h2>
<hr />
<h2 id="grant">Grant Access</h2>
<hr />
<h2 id="other">Other Access Routes</h2>
--->
