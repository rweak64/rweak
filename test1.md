
**University of Nebraska / DPAA**
|  Name| Contact Information |
|--|--|
|Pawaskar, Sachin|[spawaskar@unomaha.edu](mailto:spawaskar@unomaha.edu)

**University of Nebraska / Security Audit Team**
| Name |  Contact Information|
|--|--|
| Cernicky, Ryan |  [rcernicky@unomaha.edu](mailto:rcernicky@unomaha.edu)|
| Johns, Jordan |  [jjohns@unomaha.edu](mailto:jjohns@unomaha.edu)|
Kress, Cory|[ckress@unomaha.edu](mailto:ckress@unomaha.edu)
Navratil, Michae|[mnavratil@unomaha.edu](mailto:mnavratil@unomaha.edu)
Portz, Brennan|[bportz@unomaha.edu](mailto:bportz@unomaha.edu)
Weak, Rudy|[Rweak@unomaha.edu](mailto:Rweak@unomaha.edu)

**Project Definition and Scope**

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

-   Deliverables are to be in the form of Postman scripts.
    
-   Findings are to be documented and placed into the client’s GitHub repository at  github.com/spawaskar-cora/cora-pentest-sp20
    

**Out of Scope**

-   Social engineering the development team
    
-   Attacking the Amazon Webservices server supporting the application
    
-   Attacking the virtual machine running the server
    
-   Attacking the production environment

**CoRA System  Description**

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

![enter image description here](https://github.com/rweak64/rweak/blob/master/cora.PNG?raw=true)

**REST API**

Laravel

**Data Storage and Retrieval**

--mysql— (model)

**Service View Representation**

--javascript—  (view / user facing)

**API and Application Security**

---user authentication and authorization and identity management---

---JSON Web Tokens and Session Tracking---

---Cross-Site Request Forgery protection---

--- site / user / organization roles and permissions ---

**Client Security Expectations**

Data integrity is the main expectation our client has. It is essential that no threat actor will be able to change the data. This is what our team will focus on; making sure no vulnerabilities exist in the CoRA system that will allow unintended changing of data.

Due to the nature of the application, being hosted by a government agency, there are a plethora of threat actors. Ranging from a nation wanting to deface the site to a random vandal that just wants to test their skills. These are the main threat actors we believe  that will attack this system.

**Threat Actors**

-   Intellectual Property Thief
    
-   Unregistered/Malicious Users
    

-   Vandals
    
-   Nation State Agents
    
-   Malicious/Disgruntled Insider
    
-   Phished Employee

**Recon Material**

The reconnaissance for our project started with information that was publicly available.  We started at the login page and looked for any packages/code we could find to start looking for vulnerabilities.  Reconnaissance was done over what CoRA is and seeing if we could find any available information on the internet.  A diagram was found listing some services it uses. Recently we got login credentials so we will start testing the web API with the help of Postman and other tools to help uncover findings.

The actionable items we have found so far are listed below. They are currently all JavaScript  packages and we will do more research and testing to see if any of these packages bear any findings.

**JavaScript  Packages**

| Package Name | Version |Description
|--|--|--|
| Bootstrap|4.3.1  |A GUI
|jQuery|3.3.1|jQuery is a lambda based function expression engine for the Javascript language
|Popper|1.14.7|Popper provides easy to use methods of creating browser popup dialogue windows.
|Select2|4.0.5|Select2 is a jQuery based replacement for select boxes. It supports searching, remote data sets, and infinite scrolling of results.
|Datatables|1.10.18|It is a highly flexible tool, built upon the foundations of progressive enhancement, that adds all of these advanced features to any HTML table.
|Vue.js|2.6.10|Vue. js is actually a JavaScript framework with various optional tools for building user interfaces.
|Chart.js|2.7.2|Chart.js is a JavaScript library that allows you to draw different types of charts by using the HTML5 canvas element. Since it uses canvas, you have to include a polyfill to support older browsers.


*Ongoing Reconnaissance*

While the team made a few early discoveries about CoRAs web application the ongoing recon will dive deeper into the web  API that is used for the backend of the application.  This section of the document will get updated with new findings to help detail the findings of the app.

**Product Backlog**

**Spikes**

*Client*

-   As a user there seems to be a learning curve on  the application to get data back. We would like to have a meeting with the client to better understand the screens we will be testing, and how to test them.
    

-   Supplementary meeting with the client.
    

*Tools*

-   As a pen tester we need to set up and become familiar with pen testing tools that not all of us have used. BurpSuite will allow us to find hidden URL’s and help find vulnerabilities  to begin.
    

-   Setup and become familiar with BurpSuite
    

-   As a pen tester we need to set up and become familiar with pen testing tools that not all of us have used. Postman is required for us to use and we must submit all scripts through this.
    

-   Setup and become familiar with Postman
    

-   As a pen tester we need to set up and become familiar with pen testing tools that not all of us have used. Fiddler will allow us to find hidden URL’s and help find vulnerabilities to begin.
    

-   Setup and become familiar with Fiddler
    

*Vulnerabilities*

-   A threat actor can see this package and find vulnerabilities  within. If exploited  this could lead to unintended  consequences like allowing XSS.
    

-   Examine “Jquery - 3.341” package
    

-   A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.
    

-   Examine “Popper - 1.14.7” package
    

-   A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.
    

-   Examine “Bootstrap - 4.3.1” package
    

-   A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.
    

-   Examine “Select2 - 4.0.5” package
    

-   A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.
    

-   Examine “Jquery  DataTables - 1.10.18” package
    

-   A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.
    

-   Examine "Bue – 2.6.10” package
    

-   A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.
    

-   Examine “chart.js - 2.7.2” package
    

-   A threat actor can see this package and find vulnerabilities within. If exploited this could lead to unintended consequences like allowing XSS.
    

-   Examine “Google Tag Manager” package

**Stories**

All of these stories were requirements given to us by our customer.

**Required Stories**

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
    

**Nice to Haves**

These stores are not required for us to do but were listed as things we can do if we have enough time.

*Isotope Screens*

-   Create Isotope
    
-   View/Edit Isotope
    

*Isotope Batch Screens*

-   Create Isotope Batch
    
-   Process Isotope Batch

**Burn down Chart**

Our first Sprint we are going to try for this burn down then go from there.
![enter image description here](https://github.com/rweak64/rweak/blob/master/coraburn.PNG?raw=true)
