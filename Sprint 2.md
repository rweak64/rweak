
# CoRA API Security Audit - 2020
### Project Contact Information

**Client Point of Contact** 
|Name | Contact |
|--|--|
|Pawaskar, Sachin| spawaskar@unomaha.edu  |

**Team Contact Information** 

|Name | Contact |
|--|--|
|**Cernicky, Ryan**| **rcernicky@unomaha.edu** |
|Johns, Jordan| jjohns@unomaha.edu |
|Kress, Cory| ckress@unomaha.edu |
|Navratil, Michael| mnavratil@unomaha.edu |
|Portz, Brennan| bportz@unomaha.edu |
|Weak, Rudy| rweak@unomaha.edu |



**Sprint 2**

This is the second completed iteration of the 2020 CoRA API security audit. The following document discusses the tasks planned, accomplished, and unfinished. Findings in this report are preliminary and may or may not be reflected in the final deliverable. Sprint tasks and security goals are currently limited to auditing the CoRA application API directly.

 **Sprint Summary:**

During this sprint, the team split off into pairs to work on generating Postman Scripts for the User, Report, and Project Screens on the CoRA application. These scripts can be used by the client to bring better security tests to the application. The team also wanted to address the front-end package findings and come up with suggested remediations. 

 **Primary Goals:**

The following section will dictate the purpose, motivations, structure, and organization of this iteration of this security audit sprint 2 of the CoRA web application interface. The  main focus of sprint 2 is to do the following:

-  Research remediation methods for the JavaScript libraries discovered in Sprint 1

-  Become familiar with Burpsuite & Postman integration

-  Capture requests from user, report and project screens in Burpsuite

-  Import requests into Postman for collection organization and testing

-  Create a user matrix to show affected threats.



**Sprint 1: Team Tasks**

**Completed**


The following were completed during the current sprint

-  Screen Test – User Screens

-  Screen Test – Report Screens

-  Screen Test – Project Screens

-  Select2 (4.0.5) Remediation

-  Bootstrap (4.3.1) Remediation

-  Jquery (3.3.1) Remediation

-  Investigate Postman Integration with Burpsuite

**Incomplete**

The following are tasks scheduled for this sprint which were given points and not accomplished. These tasks will rollover into the next sprint.

-  User Matrix Creation

**Sprint 2: Findings**

**Spike Remediations:**

Following the CVE’s that were found during Sprint 1, We researched remediations to said CVE’s. The remediations are listed below:

 **Bootstrap:**

- Frontend Package was found to have a CVE-2019-8331.

- Remediation: No change needed. Bootstrap Version 4.3.1 (current version) does include a fix to the found CVE.

**Select2 4.0.5:**

- Frontend Package was found to have a CVE-2016-10744.

- Remediation: Upgrade to Select2 version 4.0.13 (or at least 4.0.6) to avoid the likelihood of  cross-site scripting attacks.

**Jquery 3.3.1:**

- Frontend Package was found to have a CVE-2019-11358.

- Remediation: Upgrade to the latest version of Jquery (3.4.1) to avoid the likelihood of object modification via the "Extend" function.

**Burpsuite – Postman Integration:**

- During sprint 2 the team wanted to get an Infrastructure working for Burpsuite and Postman Integration to help with workflow but to also help create postman scripts to deliver a more reliable product to our customer. These scripts can be found in the Sprint 2 repository under the folder called “Postman Scripts”.

**Burndown Chart:**

![enter image description here](https://github.com/rweak64/rweak/blob/master/Burndown.PNG?raw=true)


 **Ongoing Reconnaissance**
 
While the team made progress with Postman-Burpsuite integration with from CoRAs web application the ongoing development of these scrips will go into Sprint 3 as we dive deeper into the web API that is used for the backend of the application to give reliable tests of the API.

> Written with [StackEdit](https://stackedit.io/).
