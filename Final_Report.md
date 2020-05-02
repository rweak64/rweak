
# CORA SECURITY AUDIT

**University of Nebraska / DPAA**  

| Name| Contact Information |  
|--|--|  
|Pawaskar, Sachin|[spawaskar@unomaha.edu](mailto:spawaskar@unomaha.edu)  
  
  
**University of Nebraska / Security Audit Team**  

| Name | Contact Information|  
|--|--|  
| Cernicky, Ryan |  [rcernicky@unomaha.edu](mailto:rcernicky@unomaha.edu)|  
| Johns, Jordan |  [jjohns@unomaha.edu](mailto:jjohns@unomaha.edu)|  
Kress, Cory|[ckress@unomaha.edu](mailto:ckress@unomaha.edu)  
Navratil, Michael|[mnavratil@unomaha.edu](mailto:mnavratil@unomaha.edu)  
Portz, Brennan|[bportz@unomaha.edu](mailto:bportz@unomaha.edu)  
Weak, Rudy|[Rweak@unomaha.edu](mailto:Rweak@unomaha.edu) 


# Executive Summary

Sachin  Pawaskar, professor of Information Systems and Quantitative Analysis at the University of Nebraska at Omaha (UNO), has partnered with the Defense Prisoner of War (POW) and Missing In Action (MIA) Accounting Agency (DPAA). The partnership has worked to create a central location for statistical resource sharing regarding the discovery and management of forensic archeological information with the purpose of identifying and recovering the remains of soldiers found in mass graves. This project provides a necessary resource for the recovery of United States service members and their international allied counterparts who were buried in mass graves.

The application titled the Commingled Remains Analytics  (CoRA) has been designed to provide interagency communications between several forensic  oriented groups and skillsets. CoRA’s immediate purpose is to identify and inventory bones to prepare them for later analysis. This later analysis uses a Specimen Level Information Management (SLIM) approach to manage the segregation of human remains into discrete and well identified individuals. The SLIM process is supported and  framed into the CoRA web application to provide a community resource for inventorying assemblages of commingled human remains. Thus, providing a method for item segregation and subsequent identification.

The CoRA set of utilities and tools runs in the web using a plethora of technologies to support its different requirements. CoRA is stored and served from the cloud via Amazon Web Services (AWS), runs Hypertext Preprocessor (PHP) to handle functions and services, utilizes PostgreSQL for models and data storage along with a number of HTML and JavaScript technologies to present this information to the users.

CoRA’s functional controller infrastructure is built on the PHP framework known as Laravel. Laravel provides an ease of development template and common (standard) methods for handling HTTP(S) request’s and responses. The structure of the application follows the basic Model-View-Controller (MVC) paradigm which provides for a simple Web Application Programming Interface (Web API). CoRA’s web API, along with its presentation and view layer provides a simple way for forensic scientists in the lab and in the field to review, study, and classify forensic information regarding commingled remains.

Development of CoRA has been accomplished by several student teams lead by the leadership of Sachin  Pawasker, UNO and the DPAA. The requirement of continued security auditing drives this iteration of testing on the CoRA platform and will also be performed by a student team lead and organized by Sachin Pawasker and Professor Robin Gandhi at UNO.

Essential to the mission of discovering and segregating commingled remains into discrete individuals is the security of the mission of the DPAA and the partnership they have with both UNO, the forensic scientists involved, and Sachin  Pawasker. Previous iterations of security auditing have been performed by teams directly associated with the student lead project and teams of students within the Cybersecurity Degree program at UNO.

This document is an outline of the current iteration of performant security auditing to be accomplished by a student organized team from UNO. The team will be focused on the auditing of CoRA’s web API and will be testing the application using various software tools either made available to them or freely available on the open internet.

The current security team intends to perform the security audit process as managed and organized by the Agile SCRUM methodology. Each part of the project will be subdivided amongst the individual team members and organized in a sprint by sprint basis. Documents including findings, discoveries, vulnerabilities, protentional exploits, and suggested secure resource development will be included in forthcoming agile iterations and ultimately the final project report.


## Project Definition and Scope
  

The following section will dictate the purpose, motivations, structure, and organization of this iteration of security audits of the CoRA web application programming interface.  
  

**Purpose**  
  

Sachin Pawasker of UNO and the DPAA have developed a system to segregate bones found in mass graves and to classify them for possible definition as individuals. The project is the result of a direct partnership between the DPAA and UNO via Sachin Pawasker. This project provides a necessary resource for the recovery of United States service members and their international allied counterparts who were buried in mass graves.  
  

**Motivation**  
  

The CoRA application has been designed to provide interagency communications between several forensic oriented groups and skillsets. Due to the purpose of CoRA, protection of the forensic process is an essential part of providing legitimate and provable segregation of human remains. Ultimately, any and all data stored within the CoRA application must remain untouched unless required or performed by a well credentialed individual or team of individuals.  
  

Maintaining the security of CoRA through the protections of data integrity, the denial of unauthorized access to the system and maintaining system availability will be essential to supporting the DPAA’s mission of recovering service members and hopefully reuniting them with their families and country of origin.  
  

**Approach**  
  

A student led, Agile organized, team will perform a series of iterative security tests against and for the CoRA web API. System and security information will revolve around a full spectrum analysis of the system as would be performed by both foreign and internal threat actors. Specific system controller and data architectures will not be made privy to the team. The team will be provided with individual accounts spanning the entirety of possible users, groups and  permissions.  
  

Auditing the CoRA software suite will include auditing client-side scripts, verifying file integrities, attempting internal privilege escalations, and finally reporting findings in a coherent way such that the client can implement plans and procedures for future implementations of protective measures.  
  

**Project Requirements**  
  

Our client wants the team to use Postman to analyze the application and test specific screens. Screens are being used as a term for specific web pages that accept input into the server.  
  

**Rules for the Project**  
  

Client has request that project deliverables be submitted to a private git repository hosted at [www.github.com](http://www.github.com/). Deliverables will include a project description and requirements document, sprint by sprint reports, and a final report of all security findings.  
  

Project deliverables will include software configuration scripts related to the software suites used for the testing process. All findings will be organized and submitted to the client as required by the project schedule. Selected software suites which will provide reports are as follows:  
  
  

**Postman**    
[https://www.postman.com/](https://www.postman.com/)  
A web API testing suite allowing the user to develop scripts which test request and response data between a client application and the API.  
  

  **Burp Suite**  [https://portswigger.net/burp](https://portswigger.net/burp)  
 Burp Suite is a leading cybersecurity auditing tool designed for the direct testing and auditing of web-based applications. It provides several automated security scanning, reporting, vulnerability discover and classification tools. It as well provides scripting to directly test injection  
  
  
  

**Out of Scope**  
  
  

Sections of the CoRA infrastructure and ecosystem have been marked as off-limits by the client. Due to various rights and privileges restrictions while interacting with development, testing, and production services residing on a public cloud service, certain precautions will need to be taken. Further, the client has requested a technology-based audit of the CoRA API which restricts the testing team from performing certain forms of attacks.  
  

Attacks which are disallowed by contract and by client include the following:  
  

-   Social engineering the development team  
    
  
-   Attacking services and infrastructures directly related to Amazon Web Services  
    
  
-   Platforms, Infrastructure, and Software Services  
    
-   Attacking the virtual machine running the server  
    
  
-   Attacking the production environment  
  
-   All production and testing servers, services, software, configurations and personnel are out of scope.  
  
  

## CoRA System  Description
  

CoRA’s  service-oriented system is hosted in the cloud-based Amazon Web Services (AWS). AWS provides multiple mechanisms to support the development, integration, implementation and serving of highly reliable web services via various cloud-based systems. AWS provides virtualized operating systems (servers) via its platform-as-a-service (PaaS) modules, networking and connectivity systems via infrastructure-as-a-service (IaaS) modules, user authentication via its Software-as-as-Service (SaaS) modules,  and software-defined integrated services architectures such as availability zones, blob storage for data, and certificate and key management authority services.  
  

The primary purpose of CoRA is to provide multiple, distributed, users the ability to interact with forensic data in a quantitative and qualitative manner. User interaction occurs through the CoRA web interface which has well defined data models, standard web programmatic function methods, and user rights and privileges separation to support the individual requirements of forensic teams involved in identifying and segregating bones into their original human counterparts.  
  

**Use-Case Oriented System Organization**  
  

*Organizations*  
  

CoRA requires the need to support the interoperation of multiple organizational bodies using a single system. To achieve this, users are first organized into organizations. Organizations may include companies, directorates, federal offices, universities, special non-governmental organizations, or private teams.  
  

Each organization can manage its own identity and its own users within the CoRA ecosystem. This functionality allows for dynamically integrating multiple organizations into CoRA. Organizations are administered by `Organization Administrators` and are sub-managed by `Organization Manager’s`.  
  

*Users*  
  

In order to support the primary functionality CoRA has developed a series of user-oriented interaction pages, subdivided and organized by resource type with functions restricted to the rights and privileges of the current active user. Users are assigned to organizations and projects. Users and user classes are stipulated by the system in the following manner:  
  

-   Organization Administrator  
    
-   Organization Manager  
    
  
-   Project Lead  
    
-   Forensic Anthropologist  
    
-   DNA Analyst  
    
-   Isotope Analyst  
  

**Projects**  
  

Individual burial sites and their specific goals and requirements are organized into units called projects. Projects are a joint operation between many organizations and many users. Each project has a well-defined purpose, geographic location, and sets of forensic evidence.  
  

**System Technology Stack**  
  

CoRA has been developed around the Representational State Transfer (REST) architecture. Users interact with functional controllers and data models through views provided to them by a series of vertically and laterally integrated technologies. REST API’s provide the ability for different technologies, applications, and endpoints to interact with the core system in a concrete and organized manner. API calls can be made from desktop workstations, tablet devices, and even smart phones.  
  

Applications can consist of native applications for Apple iOS/macOS, Android Linux, Microsoft Windows, and cross platform technologies such as web browsers. Each application makes or receives data and information via the systems REST API interface. An example of the technology organization and structure can be found in **Figure 1.**  
  

![](https://github.com/rweak64/rweak/blob/master/cora.PNG?raw=true)![enter image description here](https://github.com/rweak64/rweak/blob/master/cora.PNG?raw=true)  
  
  

**Client Security Expectations**  
  

Data integrity is the main expectation our client has. It is essential that no threat actor will be able to change the data. This is what our team will focus on; making sure no vulnerabilities exist in the CoRA system that will allow unintended changing of data.  
  

Due to the nature of the application, being hosted by a government agency, there are a plethora of threat actors. Ranging from a nation wanting to deface the site to a random vandal that just wants to test their skills. These are the main threat actors we believe  that will attack this system.  
  
  

**Recon Material**  
  

The reconnaissance for our project started with information that was publicly available.  We started at the login page and looked for any packages/code we could find to start looking for vulnerabilities.  Reconnaissance was done over what CoRA is and seeing if we could find any available information on the internet.  A diagram was found listing some services it uses. Recently we got login credentials so we will start testing the web API with the help of Postman and other tools to help uncover findings.  
  

The actionable items we have found so far are listed below. They are currently all JavaScript  packages and we will do more research and testing to see if any of these packages bear any findings.  
  

**JavaScript  Packages**  
  

| Package Name | Version |Description  
|--|--|--|  
| Bootstrap|4.3.1 |A GUI  
|jQuery|3.3.1|jQuery is a lambda based function expression engine for the Javascript language  
|Popper|1.14.7|Popper provides easy to use methods of creating browser popup dialogue windows.  
|Select2|4.0.5|Select2 is a jQuery based replacement for select boxes. It supports searching, remote data sets, and infinite scrolling of results.  
|Datatables|1.10.18|It is a highly flexible tool, built upon the foundations of progressive enhancement, that adds all of these advanced features to any HTML table.  
|Vue.js|2.6.10|Vue. js is actually a JavaScript framework with various optional tools for building user interfaces.  
|Chart.js|2.7.2|Chart.js is a JavaScript library that allows you to draw different types of charts by using the HTML5 canvas element. Since it uses canvas, you have to include a polyfill to support older browsers.  
  
  

*Ongoing Reconnaissance*  
  

While the team made a few early discoveries about CoRAs web application the ongoing recon will dive deeper into the web  API that is used for the backend of the application.  This section of the document will get updated with new findings to help detail the findings of the app.  
  

## Product Backlog
  

*Threat Actors*  
  

-   Intellectual Property Thief  
    
- Unregistered/Malicious Users   
-   Vandals  
    
-   Nation State Agents  
    
-   Malicious/Disgruntled Insider  
    
-   Phished Employee  
  

*Spikes*  
  

|Spike Name|Conversation Note  
|--|--|  
Supplementary meeting with the client.|As a user there seems to be a learning curve on the application to get data back. We would like to have a meeting with the client to better understand the screens we will be testing, and how to test them.  
Setup and become familiar with BurpSuite|As a pen tester we need to set up and become familiar with pen testing tools that not all of us have used. BurpSuite will allow us to find hidden URL’s and help find vulnerabilities to begin.  
Setup and become familiar with Postman|As a pen tester we need to set up and become familiar with pen testing tools that not all of us have used. Postman is required for us to use and we must submit all scripts through this.  
Setup and become familiar with Fiddler|As a pen tester we need to set up and become familiar with pen testing tools that not all of us have used. Fiddler will allow us to find hidden URL’s and help find vulnerabilities to begin.  
Examine “Jquery - 3.341” package|A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.  
Examine “Popper - 1.14.7” package|A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.  
Examine “Bootstrap - 4.3.1” package|A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.  
Examine “Select2 - 4.0.5” package|A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.  
Examine “Jquery  DataTables - 1.10.18” package|A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.  
Examine "Vue – 2.6.10” package|A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.  
Examine “chart.js - 2.7.2” package|A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.  
Examine “Google Tag Manager” package|A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.  
  

**Stories**  
  

*Required Stories*  
  

All of these stories were requirements given to us by our customer.  
  

See list 1 the appendix  
  

*Nice to Haves*  
  

These stores are not required for us to do but were listed as things we can  do if we have enough time.  
  

See list 2 in the appendix  
  

**See the appendixes**  
  
  

**Burn down Chart**  
  

Our first Sprint we are going to try for this burn down then go from there.  

![](https://github.com/rweak64/rweak/blob/master/coraburn.PNG?raw=true?raw=true)  
  

# Sprint 1
This is the first completed iteration of the 2020 CoRA API security audit. The following document discusses the tasks planned, accomplished, and unfinished. Findings in this report are preliminary and may or may not be reflected in the final deliverable. Sprint tasks and security goals are currently limited to auditing the CoRA application API directly.

**Sprint Summary:**
Team members discovered a number of front facing Javascript libraries which required further investigation. Discovered vulnerabilities are not labeled High-Risk. Selections of vulnerabilities related to the front-end Javascript libraries require related PHP code to be executed on the server which we do not believe exists in the application at this time. We suggest to the client that these libraries be updated regardless of this fact. Future implementations and iterations of the CoRA application could become vulnerable due to these discoveries if more complex functionality is implemented into the CoRA ecosystem. The team was unable to begin certain aspect of permissions matrix testing and verification, those requirements have been rolled into the following sprints.

**Previous accomplishments to this sprint include:**

*RECONNAISSANCE*
* Retrieve all frontend Javascript Libraries
* Discover domains and naming schemas of API
* HTTP/HTTPS verification 

*POSTMAN*
* Configured Team Collection
* Configured Login/Logout Procedures
* Basic Data and Report Retrieval  

**Primary Goals:**

The 2020 CoRA audit team has previously performed a series of initial reconnaissance tasks targeting the https://dev.coracore.com web API. Sprint 1 is an advancement of the reconnaissance (initial) phase. Team goals for sprint 1 are as follows:

* Understand the CoRA application
    * Basic Access (Login/Logout)
    * Purpose of the CoRA tool
        * Organizational Structure
        * Project Structure and Data Field's
    * API Token Usage (JWT Bearer Token)
    * User Creation, Edit, and Deletion
* Understand CoRA Application API
    * Basic Laravel web API structure
    * HTTP Request/Response format (JSON raw and/or URLEncoding)

## Sprint 1: Findings

The following is a non-exhaustive list of initial findings. Please note that findings may or may not be reflected differently in the final deliverable. 

|Package | Version |  Assigned To | Findings |
|--|--|--|--|
|jquery DataTables | 1.10.18 |Rudy Weak| No known vulnerabilities for this version of DataTables.|
|Vue |2.6.10 |Brennan Portz| I did not find any CVE's for Vue 2.6.10 or newer. All existing CVE's are for older versions that are no longer relevant.|
|Select2 |4.0.5 |Cory Kress|Here is a CVE for Select2 4.0.5. It is [https://nvd.nist.gov/vuln/detail/CVE-2016-10744](https://nvd.nist.gov/vuln/detail/CVE-2016-10744). Published on 03/27/2019. CVE-2016-10744. Looks to be legit. There is no output escaping on this select tool. So, if somehow, there is code in the form that can execute, it will. There are solutions out there for this problem. [https://github.com/snipe/snipe-it/pull/6831/commits/5848d9a10c7d62c73ff6a3858edfae96a429402a](https://github.com/snipe/snipe-it/pull/6831/commits/5848d9a10c7d62c73ff6a3858edfae96a429402a).|
|Popper | 1.14.7 |Micahel Navratil|Found that there are no known CVEs for the currently used version of Popper which is version 1.14.7|
|jquery | 3.3.1 |Micahel Navratil|  *Vulnerable module*: jquery *Vulnerable module*: jquery *Introduced through*: jquery@3.3.1 *Remediation*: Upgrade to jquery@3.4.0. *Overview* jquery is a JavaScript library. It makes things like HTML document traversal and manipulation, event handling, animation, and Ajax much simpler with an easy-to-use API that works across a multitude of browsers.Affected versions of this package are vulnerable to Prototype Pollution. The extend function can be tricked into modifying the prototype of Object when the attacker controls part of the structure passed to this function. This can let an attacker add or modify an existing property that will then exist on all objects.Prototype **Pollution vulnerability report**[https://snyk.io/test/npm/jquery/3.3.1](https://snyk.io/test/npm/jquery/3.3.1)|
|Bootstrap | 4.3.1 |Micahel Navratil| In Bootstrap before 3.4.1 and 4.3.x before 4.3.1, XSS is possible in the tooltip or popover data-template attribute.  *Integrity Impact Partial* (Modification of some system files or information is possible, but the attacker does not have control over what can be modified, or the scope of what the attacker can affect is limited.)Availability Impact None (There is no impact to the availability of the system.)  *Access Complexity Medium* (The access conditions are somewhat specialized. Some preconditions must be satistified to exploit)*Authentication Not required* (Authentication is not required to exploit the vulnerability.)**Gained Access None**  *Vulnerability Type(s) Cross Site Scripting*  *CWE ID 79*: [https://www.cvedetails.com/cve/CVE-2019-8331/](https://www.cvedetails.com/cve/CVE-2019-8331/)|
|charts.js |2.7.2 |Ryan Cernicky| No publicly known vulnerabilities were found|
|Google Tag manager | ? |Ryan Cernicky| The way that the google tag manager is implemented for this products looks as if it is just there to provide google analytics. No outside javascript is being loaded. Also only if someone compromises the GTM account to load external javascript would be the only vulnerability.|

## Sprint 1: Team Tasks

**Completed**

| Test Environment setup|Assigned to| Description |
|--|--|--|
|Postman|All Members|Look at burp suite section to learn how to integrate Postman and burp suite. Overall, with burpsuite, fairly easy to make the collections and run them. Easy enough to pass around the collections as json too, just gotta import and export.
| Burp suite |All Members| As noted, Burpsuite has postman integration and it is extremely simple. You click around with Burpsuite proxing your browser and then you can select the urls you want to export. After you have them selected you can right click and, with the postman extension downloaded, export as a postman json collection. You can then just pop into Postman and import the json. It is pretty easy to pass around the collections as json files.The website we are trying to pen test is and HTTPS server and that makes setting up burpsuite to work a little harder. We needed to download a CA cert for Burpsuite to work. Documentation from Burpsuite [https://portswigger.net/support/installing-burp-suites-ca-certificate-in-chrome](https://portswigger.net/support/installing-burp-suites-ca-certificate-in-chrome) and [https://portswigger.net/support/installing-burp-suites-ca-certificate-in-internet-explorer](https://portswigger.net/support/installing-burp-suites-ca-certificate-in-internet-explorer). Overall you need to set up your proxy, go to [http://burp](http://burp/), download the CA cert, run the file and make sure to put it into root trusted certs (at least for chrome). After that everything worked |
|Fiddler|All Members|Found it fairly easy to setup and run will probably not use that much now that we have found the burpsuite integration for postman making it much easier to work

**Incomplete**

The following are tasks scheduled for this sprint which were given points and not accomplished. These tasks will rollover into the next sprint. 

|Screen Test|assigned to|scripts|Results
|--|--|--|--|
| Specimen: Biological Profile |Cory Kress,Micahel Navratil| N/A |N/A
|Specimen: DNA|Ryan Cernicky,Rudy Weak|N/A|N/A
|Specimen: Isotope|Brennan Portz,Jordan Johns|N/A|N/A

**Sprint 1: Burn Down Chart**

![enter image description here](https://github.com/rweak64/rweak/blob/master/cap1.PNG?raw=true)


|Story|Points|Members|Time Spent|
|--|--|--|--|
|Postman|1|All members|
|Burp suite|1|All Members|
|Fiddler|1|All Members|
|jquery DataTables CVE Findings|1|Rudy Weak|
|Select2 CVE Findings|1|Cory Kress|
|Bootstrap CVE Findings|1|Micahel Navratil|
|jquery CVE Findings|1|Micahel Navratil|
|Bootstrap CVE Findings|1|Micahel Navratil|
|Google Tag manager CVE Findings|1|Ryan Cernicky|
|charts.js CVE Findings|1|Ryan Cernicky|
|Vue |1|Brennan Portz|

# Sprint 2

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



## Sprint 2: Team Tasks

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

## Sprint 2: Findings

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

|Story|Points|Members|
|--|--|--|
|Screen Test – User Screens|1|Jordan Johns,Micahel Navratil|
| Screen Test – Report Screens|1|Ryan Cernicky,Rudy Weak|
| Screen Test – Project Screens|1|Brennan Portz,Cory Kress|
|Select2 (4.0.5) Remediation|1|Micahel Navratil|
|Bootstrap (4.3.1) Remediation|1|Brennan Portz,Micahel Navratil|
|Jquery (3.3.1) Remediation|1|Brennan Portz,Micahel Navratil|
|Investigate Postman Integration with Burpsuite|1|All Members|
|User Matrix Creation-incomplete|1|Jordan Johns|

 **Ongoing Reconnaissance**
 
While the team made progress with Postman-Burpsuite integration with from CoRAs web application the ongoing development of these scrips will go into Sprint 3 as we dive deeper into the web API that is used for the backend of the application to give reliable tests of the API.








# Sprint 3

This is the third completed iteration of the 2020 CoRA API security audit. The following document discusses the tasks planned, accomplished, and unfinished. 
Findings in this report are preliminary and may or may not be reflected in the final deliverable. Sprint tasks and security goals are currently limited to auditing the CoRA application API directly.



 **Sprint Summary:**
 During this sprint, the team split off into pairs to work on generating Postman Scripts for the following screens: Search, DNA, and Administration Screens residing in inside the CoRA application. 
 These scripts are to be used by the client to bring better security test audits to the CoRA application. 
 The team also wanted to do some additional scanning and was tasked to use OWASP ZAP to scan the website for additional vulnerabilities.

  **Primary Goals:**

The following section will dictate the purpose, motivations, structure, and organization of this iteration of this security audit sprint 3 of the CoRA web application interface. The main focus of sprint 3 is to do the following:

- Change the Existing request to use CSRF tokens for Authentication

- Capture requests from Search, DNA, and Administration Screens in Burp suite

- Import requests into Postman for collection organization and testing

- Become familiar with OWASP ZAP and scan the website for vulnerabilities

## Sprint 3: Team Tasks

**Completed**
The following were completed during the current sprint
 
+ **Screen-Test | Administration Screens**
    - Members: Michael, Brennan
    - Points:1
    - Conversations:
        - Required to be tested by the customer
	- Acceptance Criteria:
		- All Admin Screens will be tested on Burpsutie.
		- All Admin Screens will be exported to Postman.
		- All Admin Screens-export will be stored into their own collection within Postman.
		- All Collections will be tested with Authentication.
 
 
+ **Screen-Test | Search Screens**
    - Members: Ryan, Cory, Michael
    - Points:1
    - Conversations:
        - Required to be tested by the customer
	- Acceptance Criteria:
		- All Search Screens will be tested on Burpsutie.
		- All Search Screens will be exported to Postman.
		- All Search Screens-export will be stored into their own collection within Postman.
		- All Collections will be tested with Authentication.

		
+ **Screen-Test | DNA Screens**
    - Members: Rudy, Brennan
    - Points:1
    - Conversations
        - Required to be tesetd by the customer
	- Acceptance Criteria:
		- All DNA Screens will be tested on Burpsutie.
		- All DNA Screens will be exported to Postman.
		- All DNA Screens-export will be stored into their own collection within Postman.
		- All Collections will be tested with Authentication.

		
+ **Setup and Familiarization with ZAP**
    - Members: All members
    - Points:1
    - Conversation:
        - As a security engineer, it is essential to use a tool like zap to understand the layout of a network. Zap can 
        also automatically scan the endpoints of the system and do analysis against them to find vulnerabilities.
	- Acceptance Criteria:
		- All members will download ZAP.
		- All members will login to the applicaiton using ZAP as its proxy.
		- All members will run scans using the ZAP applicaiton.

		
+ **SPIKE: User Authentication using CSRF Token**
    - Members:Jordan,Cory
    - Points:1
    - Conversations:
        - During Sprint 2 demo revealed that the PO wants us to authenticate with the application using the CSRF token instead of going through the API and using the Bearer token at this time. We will rework our collection scripts to reflect such change.
        This spike is to rework the environmental variables we have set in our collections to use the correct form of authentication. 
	-Acceptance Criteria:
		- Authentication for collections will grab and store each users CSRF token.
		- Authenticaion will work for newly created collection and legacy collections.

     

## Sprint 3: Findings

+ **Screen-Test | Administration Screens**
    - Found and tested the Haplogroup Management, Accession and Instrument screens.
    - Could not find the Tag Management screen.
        

+ **Screen-Test | Search Screens**
    - On the Reports Screens, if you are logged in as an isotope analyst, there is a report option called MTDNA
      that fails to load. A webpage error occurs when you click on it. The path for this error is: 
        https://cora-dev.herokuapp.com/reports/mtdna. This does work for the DNA analyst.
    - Could only find eleven report screens and not all fifteen that were required. 

+ **Screen-Test | DNA Screens**
    - Found when creating a POST request for the DNA Screens, there are extra numbers in the url that have been found to be the DNA Specimen ID
    - This is in conjunction with the Specimen ID being present in the url as well when editing a DNA file
    - Found that a user can also navigate by changing the DNA specimen ID number and the Specimen ID number in the url which is not secure 

+ **ZAP scan**
  - Found there were no major vulnerabilities that were found from a scan finished on 4/13/2020, a more indepth look into the application will be done in sprint 4

+ **SPIKE: User Authentication using CSRF Token**
    - Switched from using Bearer tokens to using CSRF tokens as requested by PO.
    - The team made a template for using CSRF tokens in our Postman Scripts.

**Burndown Chart:**

![enter image description here](https://github.com/spawaskar-cora/cora-pentest-sp20/blob/master/Sprint%203/BurnDownChart.png?raw=true)

|Story |Points |Members |
|--|--|--|
|Administration Screens|1|Michael,Brennan|
|Search Screens|1|Ryan,Cory,Michael|
|DNA Screens|1|Rudy, Brennan|
|Setup and Familiarization with ZAP|1|All members|
|User Authentication using CSRF Token|1|Jordan,Rudy,Cory|


**Ongoing Reconnaissance**
- Jquery and Bootstrap have an upgrade. jQuery 3.5.0 Released. This addresses a Security Fix that was found with jQuery.htmlPrefilter method. the  issue was reported that demonstrated the regex could introduce a cross-site scripting (XSS) vulnerability. discussed on their blog 
   blog.jquery.com/2020/04/10/jquery-3-5-0-released Besides this. There are no current vulnerabilites in the versions being used by the CoRA application.
- Two users are not being tested as the password has either expired or the users have been deleted off the system. This issue will be brought up to the PO during product demo.

**Planned Sprint 4 Tasks**

Sprint 4 is the final sprint for this capstone. The planned work for this sprint will consist of a story of creating the User Matrix to better outline what risks each user type bring to the applicaiton,
the finalization of collecting screens for the specimens page, and perform a more indepth look into ZAP and the different findings it presents us with. A table of the stories we wish to work on will be below:

|Story | Points | Members |
|--|--|--|
|User Matrix Creation|1| Ryan, Jordan|
|Specimen Screens|1| Cory, Michael, Brennan, Rudy|
|Analysis of ZAP Findings|1| Everyone|
|Administration Screens|1| Michael, Brennan|
|Setup and Familiarization with ZAP|1|All members|

# Sprint 4

This is the forth completed iteration of the 2020 CoRA API security audit. The following document discusses the tasks planned, accomplished, and unfinished. 
Findings in this report are preliminary and may or may not be reflected in the final deliverable. Sprint tasks and security goals are currently limited to auditing the CoRA application API directly.



 **Sprint Summary:**
 During this sprint, the team split off into pairs to work on generating Postman Scripts for the following screens: Isotope and Specimens Screens residing in inside the CoRA application. 
 These scripts are to be used by the client to bring better security test audits to the CoRA application. 
 The team also wanted to do some additional scanning and was tasked to use OWASP ZAP to scan the website for additional vulnerabilities.

  **Primary Goals:**

The following section will dictate the purpose, motivations, structure, and organization of this iteration of this security audit sprint 4 of the CoRA web application interface. The main focus of sprint 4 is to do the following:


- Capture requests from Isotope and Specimen in Burp suite

- Become familiar with OWASP Zap Findings and Reccomend mitigations.

## Sprint 4: Team Tasks

**Completed**
The following were completed during the current sprint
 
+ **Screen-Test | Isotope Screens**
    - Members: Rudy
    - Points:1
    - Conversations:
        - Required to be tested by the customer
	- Acceptance Criteria:
		- All Isotope Screens will be tested on Burpsutie.
		- All Isotope Screens will be exported to Postman.
		- All Isotope Screens-export will be stored into their own collection within Postman.
		- All Collections will be tested with Authentication.
 
 
+ **Screen-Test | Specimens Screens**
    - Members: Rudy, Micheal, Cory, Brennan
    - Points:1
    - Conversations:
        - Required to be tested by the customer
	- Acceptance Criteria:
		- All Specimens Screens will be tested on Burpsutie.
		- All Specimens Screens will be exported to Postman.
		- All Specimens Screens-export will be stored into their own collection within Postman.
		- All Collections will be tested with Authentication.


		
+ **Analysis of Zap Findings**
    - Members: All members
    - Points:1
    - Conversation:
        - As a security engineer, it is essential to use a tool like zap to understand the layout of a network. Zap can 
        also automatically scan the endpoints of the system and do analysis against them to find vulnerabilities. With these vulnerabilities found good reccomendations to mitigate should be presetned to the Product Owners.
	- Acceptance Criteria:
		- All members will run scans using the ZAP applicaiton.
		- All members will compile a list of findings.
		- All members will research said findings against the MITRE CWE.

     

## Sprint 4: Findings

+ **Screen-Test | Isotope Screens**
    - All screens under the Isotope category were collected and all are working and testable.
        

+ **Screen-Test | Specimens Screens**
    - All screens under the Isotope category were collected and all are working and testable.
	- Some errors were encountered when submitting a post request about 10% of the time testing.

+ **ZAP scans**
  - A single high threat vulnerability was found by the ZAP scans. It resulted in a Path Traversal Vulnerability. When talking to the product owner about this, they knew about the finding and said that it is the result of using Amazon Web Services for the infrastructure.



**Burndown Chart:**

![enter image description here](https://github.com/spawaskar-cora/cora-pentest-sp20/blob/master/Sprint%204/Sprint_4.png?raw=true)

|Story |Points |Members |
|--|--|--|
|Isotope Screens|1|Rudy|
|Specimens Screens|1|Rudy, Micheal, Cory, Brennan|
|Setup and Familiarization with ZAP|1|All members|


**Ongoing Reconnaissance**
- The two users that was brought up at the last demo of having incorrect account info, thus not being able to log into the system was mitigated by the Product Owner. These user roles have yet to be implemented on the system and that was the reason why we could not log in as them. 


**Appendix**  
  
  
*list 1:*  
  

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
    
-   15 Reports screens  
    
  

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
    
  

*list 2:*  
  

*Isotope Screens*  
  

-   Create Isotope  
    
-   View/Edit Isotope  
    
  

*Isotope Batch Screens*  
  

-   Create Isotope Batch  
    
-   Process Isotope Batch  


