

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

**Sprint 3**

This is the third completed iteration of the 2020 CoRA API security audit. The following document discusses the tasks planned, accomplished, and unfinished. Findings in this report are preliminary and may or may not be reflected in the final deliverable. Sprint tasks and security goals are currently limited to auditing the CoRA application API directly.



 **Sprint Summary:**
 During this sprint, the team split off into pairs to work on generating Postman Scripts for the Search, DNA, and Administration Screens on the CoRA application. These scripts can be used by the client to bring better security tests to the application. The team also wanted to do some additional scanning and was tasked to use OWASP ZAP to scan the website for additional vulnerabilities  

  **Primary Goals:**

The following section will dictate the purpose, motivations, structure, and organization of this iteration of this security audit sprint 3 of the CoRA web application interface. The  main focus of sprint 3 is to do the following:

- Change the Existing request to use CSRF tokens for Authentication

- Capture requests from Search, DNA, and Administration Screens in Burp suite

-  Import requests into Postman for collection organization and testing

-  Become familiar with OWASP ZAP and scan the website for vulnerabilities

**Sprint 3: Team Tasks**

**Completed**
The following were completed during the current sprint
 
-  **Screen-Test | Administration Screens**
- Members
- Michael,Brennan
- Conversations
 
-  **Screen-Test | Search Screens**
- Members
- Ryan,Cory,Michael
- Conversations 

- **Screen-Test | DNA Screens**
- Members
- Rudy, Brennan
- Conversations 

-   **Setup and Familiarization with ZAP**
- Members
- All members
- Conversations 

-  **SPIKE: User Authentication using CSRF Token**
- Members
- Jordan,Rudy,Cory
- Conversations 

**Sprint 3: Findings**

  **ZAP scan**
  
 - found that there where no major vulnerabilities that where found when the scan was run on 4/13/2020
 
**Screen-Test | DNA Screens**

- found that when creating post request for DNA there are extra numbers in the url that have been found to be the DNA Specimen ID

- This is in conjunction with the Specimen id being present in the url as well when editing a DNA file

- found that you can also navigate by changing the DNA specimen id number and the Specimen id number in the url which is not secure

**SPIKE: User Authentication using CSRF Token**

**Burndown Chart:**
|Story|Points|Members|Time Spent|
|--|--|--|--|
|Administration Screens|1|Michael,Brennan|
|Search Screens|1|Ryan,Cory,Michael|
|DNA Screens|1|Rudy, Brennan|
|Setup and Familiarization with ZAP|1|All members|
|User Authentication using CSRF Token|1|Jordan,Rudy,Cory|


  **Ongoing Reconnaissance**
  
