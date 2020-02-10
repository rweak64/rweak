

## Project Definition and Scope

**Project Point of Contact Information**
|  Name| Contact Information |
|--|--|
|Pawaskar, Sachin|[spawaskar@unomaha.edu](mailto:spawaskar@unomaha.edu)

**Security Audit Team**
| Name |  Contact Information|
|--|--|
| Cernicky, Ryan |  [rcernicky@unomaha.edu](mailto:rcernicky@unomaha.edu)|
| Johns, Jordan |  [jjohns@unomaha.edu](mailto:jjohns@unomaha.edu)|
Kress, Cory|[ckress@unomaha.edu](mailto:ckress@unomaha.edu)
Navratil, Michae|[mnavratil@unomaha.edu](mailto:mnavratil@unomaha.edu)
Portz, Brennan|[bportz@unomaha.edu](mailto:bportz@unomaha.edu)
Weak, Rudy|[Rweak@unomaha.edu](mailto:Rweak@unomaha.edu)

**Client Product  Description**
The application is a web app  that supports Anthropologists, DNA Analysts and Isotope Analysts  of the Defense POW/MIA Accounting Agency or DPAA. It allows them to log bones of deceased soldiers and information about how they died. The reason for this is to help find out who the bones of the deceased soldier belong to and help find their story.

This application allows 6 types of users on the system.

**User Groups:**

 - Anthropologist
 - DNA Analyst
 - Isotope Analyst
 - Project Lead
 - Org Administrator
 - Org Manager

The Anthropologist, DNA Analyst and Isotope Analyst are allowed to do different things (ex. add bones to a person) related to their expertise and are not allowed to touch the other areas. The latter three user groups can manage projects on the app; some are allowed to create and delete projects as well.

**Project Requirements**
Our client wants our team to use Postman to go through the application and test certain screens. Screens just being a term for specific web pages that allow input into the server.

**Rules for the Project**
All delivered scripts should be Postman scripts
Document any finding to be submitted to the client in the posted GitHub repository

github.com/spawaskar-cora/cora-pentest-sp20

**Screens to Test:**

*Specimens Screens*

-   Create Specimen    
-   View/Edit Specimen    
-   Specimen - Biological Profile    
-   Specimen - DNA
-   Specimen - Isotope   
-   Specimen - Taphonomy    
-   Specimen - Zones
-   Specimen - Measurements   
-   Specimen - Articulation
-   Specimen - Pair Matching    
-   Specimen - Refits    
-   Specimen - Morphology 
-   Specimen - Pathology
-   Specimen - Trauma
-   Specimen - Anomaly
-   Specimen Review
-   Create Specimen By Bone Group

*DNA Screens*
-   Create DNA
-   View/Edit DNA

*User Screens*
-   User Management Screens
-   User Profile

*Project Screens*
-   Project Management Screens  
-   Project Profile

*Reports Screens*
-   Reports Dashboard 
-   All 15 Reports screens

*Search Screens*
-   Specimen Search  
-   DNA Search 

*Administration Screens*
-   User Management Screens 
-   Project Management Screens
-   Accession Management Screens 
-   Instrument Management Screens
-   Haplogroup Management Screens
-   Tag Management Screens

*Data API for Analytics*
-   Specimen Articulations
-   Specimen Pair Matching
-   Specimen Associations 
-   Individual Specimens

Our client also has “Nice to Haves” if we get far enough in this semester.

**Nice to Haves Screens:**

*Isotope Screens*

-   Create Isotope 
-   View/Edit Isotope

*Isotope Batch Screens*
-   Create Isotope Batch  
-   Process Isotope Batch

**Client Security Expectations**

*Threat Actors*
-   Intellectual Property Thief    
-   Unregistered/Malicious Users   
-   Terrorism  
-   Nation State Warfare
-   Malicious Insider
-   Phished Employee

*Stake Holders*
-   Sachin  Pawaskar – Product Owner
-   Dr. Ghandi – Lead Capstone Mentor

**Out of Scope**
-   Social engineering the development team
-   Attacking the Amazon Webservices server supporting the application
-   Attacking the virtual machine running the server
-   Attacking the production environment

**CoRA Core Infrastructure**

From what the client has told us, their application runs on a cloud-based server that is hosted by Amazon Web Services. CoRA’s server API is something we could end up testing, but for now we are just going to be testing the web API. The web API is written in Laravel and is talked to by a web application. The web application is written in JavaScript.

The web API and the web app are the two thing we are going to be focusing on the most. We are going to be trying to find the JavaScript packages being used and look for vulnerabilities in them. There are a lot of vulnerabilities that can be found this way, the main ones we are looking for is XSS or CSRF. This could allow a malicious user to find ways to masquerade as a different user and do malicious activities or they could send benign users to malicious webpages.

Laravel, again, is what the web  API is written in. This is what is going to be doing most of the input cleansing and output escaping. If we find vulnerabilities in this code, it could lead to a plethora of vulnerabilities like allowing SQL Injection.

**Design/Network Diagram**


![Network diagram design](https://github.com/rweak64/rweak/blob/master/cora.PNG?raw=true)

**Recon Material**

During the reconnaissance period of our investigation of the CoRA website; our team started with information that was publicly available to us. While the public information is just a starting point for the team, we will branch into other aspects of the web application. Eventually testing the server API with the help of Postman and other tools will help uncover findings.

Within the early part of our recon, we were able to outline a few different technologies that were used to create CoRAs  website. The outline below will show what has been discovered and what we know about them.

**Front End**

*Javascript Packages*
| Package Name | Version |Description
|--|--|--|
| Bootstrap|4.3.1  |A GUI
|jQuery|3.3.1|jQuery is a lambda based function expression engine for the Javascript language
|Popper|1.14.7|Popper provides easy to use methods of creating browser popup dialogue windows.
|Select2|4.0.5|Etc
|Datatables|1.10.18|Etc
|Vue.js|2.6.10|Etc
|Chart.js|2.7.2|Etc

Laravel

AWS

The CoRAs Web application is host on AWS and is a distributed site with cloud-based functions

Ongoing Reconnaissance

While the team made a few early discoveries about CoRAs web application the ongoing recon will dive deeper into the server API’s that are used for the backend of the app.  This section of the document will get updated with new findings to help detail the findings of the app.

**Audit Backlog**

*Client:*

-   Supplementary meeting with the client.

*Programs:*

-   Setup and become familiar with Burpsuite
-   Setup and become familiar with Postman
-   Setup and become familiar with Fiddler

*Spikes:*

-   Examine “Jquery - 3.341” package   
-   Examine “Popper - 1.14.7” package
-   Examine “Bootstrap - 4.3.1” package 
-   Examine “Select2 - 4.0.5” package
-   Examine “Jquery DataTables - 1.10.18” *package*
-   Examine "Bue – 2.6.10” package
-   Examine “chart.js - 2.7.2” package
-   Examine “Google Tag Manager” package

*Vulnerabilities:*

-   Need to find where these live. I believe Pawar gave us a link?
