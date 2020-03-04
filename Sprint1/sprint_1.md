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

# Sprint 1
This is the first completed iteration of the 2020 CoRA API security audit. The following document discusses the tasks planned, accomplished, and unfinished. Findings in this report are preliminary and may or may not be reflected in the final deliverable. Sprint tasks and security goals are currently limited to auditing the CoRA application API directly.

## Sprint Summary: 
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

## Primary Goals:
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

# Sprint 1: Team Tasks
## Completed
| Test Environment setup|Assigned to| Description |
|--|--|--|
|Postman|All Members|Look at burp suite section to learn how to integrate Postman and burp suite. Overall, with burpsuite, fairly easy to make the collections and run them. Easy enough to pass around the collections as json too, just gotta import and export.
| Burp suite |All Members| As noted, Burpsuite has postman integration and it is extremely simple. You click around with Burpsuite proxing your browser and then you can select the urls you want to export. After you have them selected you can right click and, with the postman extension downloaded, export as a postman json collection. You can then just pop into Postman and import the json. It is pretty easy to pass around the collections as json files.The website we are trying to pen test is and HTTPS server and that makes setting up burpsuite to work a little harder. We needed to download a CA cert for Burpsuite to work. Documentation from Burpsuite [https://portswigger.net/support/installing-burp-suites-ca-certificate-in-chrome](https://portswigger.net/support/installing-burp-suites-ca-certificate-in-chrome) and [https://portswigger.net/support/installing-burp-suites-ca-certificate-in-internet-explorer](https://portswigger.net/support/installing-burp-suites-ca-certificate-in-internet-explorer). Overall you need to set up your proxy, go to [http://burp](http://burp/), download the CA cert, run the file and make sure to put it into root trusted certs (at least for chrome). After that everything worked |
|Fiddler|All Members|Found it fairly easy to setup and run will probably not use that much now that we have found the burpsuite integration for postman making it much easier to work

## Incomplete
The following are tasks scheduled for this sprint which were given points and not accomplished. These tasks will rollover into the next sprint. 
|Screen Test|assigned to|scripts|Results
|--|--|--|--|
| Specimen: Biological Profile |Cory Kress,Micahel Navratil| N/A |N/A
|Specimen: DNA|Ryan Cernicky,Rudy Weak|N/A|N/A
|Specimen: Isotope|Brennan Portz,Jordan Johns|N/A|N/A

## Sprint 1: Burn Down Chart
![enter image description here](https://github.com/rweak64/rweak/blob/master/cap1.PNG?raw=true)
