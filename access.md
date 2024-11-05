---
title: Access
subtitle: Get access to JADE HPC facilities
layout: page
permalink: "/access/"
---

<hr />
<h2 id="simple">JADE Important Service Information</h2>

We would like to take the opportunity to remind you of the agreed timetable for the phased withdrawal of the JADE-2 Service.  

This timetable has been agreed between University of Oxford (Professor Wes Armour), STFC Hartree Centre and representatives for the JADE community:

<li>From 1st September 2024: No new groups or user accounts will be provisioned on the system.</li>
<li>From 15th November 2024: Batch and interactive access to all compute resources will be withdrawn. [1]</li>
<li>6th January 2025: All access to the service will be withdrawn and physical decommissioning of the system will commence.</li>
<br>

[1] Extended from the previously announced date of 1st November 2024. 

At 4pm on Friday 15th November 2024, all job partitions (queues) will be set to "Inactive" thereby prohibiting job submission. Any jobs already dispatched at that time will run to completion but all "pending" jobs will be cancelled. 

<b>Please be advised that vendor-based support for JADE-2's hardware components, including its primary storage appliance, has ended. Consequently, the service should now be considered “at risk”.

Although it is intended that the system remains on-line through January 2025 to facilitate the retrieval of data, users are reminded of the urgency with which they should now attend to the migration of required files to a secondary location outside of JADE-2.</b>

To accompany the withdrawal of the compute service for JADE-2, the level of corresponding user support available from the Hartree Centre will also reduce in scope and will focus on supporting users with their access to the system and to their data only.

Note: Following the closure of the original "JADE" system (later referred to as "JADE-1" following the introduction of the "JADE-2" system), the newer "JADE-2" system is now the only system providing the "JADE" service. 

With regard to continued GPU resource access, you should in the first instance check with your local insitutional RSE representitive, as listed on the <a href="https://www.jade.ac.uk/support/">Support</a> page.

<!--- Old text

<h2 id="simple">Introduction</h2>

As agreed with EPSRC, the use of JADE is to be split approximately 50:30:20 between Machine/Deep Learning (ML), Molecular Dynamics (MD), and other applications, with up to 10% of the use being for research in non-EPSRC areas.

JADE is particularly intended for applications using up to 8 GPUs with a very high performance NVlink interconnect.  It is not designed for MPI applications spanning multple compute nodes; for this purpose users should apply to use a more appropriate CPU/GPU Tier 2 system. Further details of these systems can be found [here](https://epsrc.ukri.org/research/facilities/hpc/tier-2-hpc-centres)

#### Machine Learning ####

Researchers in partner universities should contact their [local RSE support](http://www.jade.ac.uk/support/) or <a href="mailto:wes.armour@oerc.ox.ac.uk">Prof Wes Armour</a>.

Researchers from other universities should apply for time through the twice-yearly [EPSRC Tier 2 RAP (Resource Allocation Panel)](https://www.ukri.org/councils/epsrc/facilities-and-resources/using-epsrc-facilities-and-resources/apply-for-access-to-high-performance-computing-facilities/)

Tier 2 RAP Technial Assessments for JADE should be sent to: [ResearchComputePlatforms@turing.ac.uk](mailto:ResearchComputePlatforms@turing.ac.uk)


Pump-priming time will also be available; please contact <a href="mailto:wes.armour@oerc.ox.ac.uk">Prof Wes Armour</a> in the first instance.


#### Molecular Dynamics ####

Time for Molecular Dynamics applications will only be allocated via the [HECBioSim](http://www.hecbiosim.ac.uk/) consortium.


<hr />
<h2 id="simple">Academic Access</h2>

To obtain a user account you need:

* a Hartree Centre Self Service Portal (Service Now) Account;
* a [Hartree SAFE account](https://um.hartree.stfc.ac.uk/hartree/signup.jsp);
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
ssh -l xyz-abc jade2.hartree.stfc.ac.uk
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
