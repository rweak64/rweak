
## Sprint 1

|Java Package name| CVE Description |
|--|--|
| jquery DataTables 1.10.18  |  found that there are no known CVEs for the currently used version of jquery DataTables which is version 1.10.18|
|Select2 4.0.5|There is a CVE for Select2 4.0.5. It is [https://nvd.nist.gov/vuln/detail/CVE-2016-10744](https://nvd.nist.gov/vuln/detail/CVE-2016-10744). Published on 03/27/2019. CVE-2016-10744. Looks to be legit. There is no output escaping on this select tool. So, if somehow, there is code in the form that can execute, it will. There are solutions out there for this problem. [https://github.com/snipe/snipe-it/pull/6831/commits/5848d9a10c7d62c73ff6a3858edfae96a429402a](https://github.com/snipe/snipe-it/pull/6831/commits/5848d9a10c7d62c73ff6a3858edfae96a429402a). 
|Popper 1.14.7|found that there are no known CVEs for the currently used version of Popper which is version 1.14.7
|jquery@3.3.1  | *Vulnerable module*: jquery *Vulnerable module*: jquery *Introduced through*: jquery@3.3.1 *Remediation*: Upgrade to jquery@3.4.0. *Overview* jquery is a JavaScript library. It makes things like HTML document traversal and manipulation, event handling, animation, and Ajax much simpler with an easy-to-use API that works across a multitude of browsers.Affected versions of this package are vulnerable to Prototype Pollution. The extend function can be tricked into modifying the prototype of Object when the attacker controls part of the structure passed to this function. This can let an attacker add or modify an existing property that will then exist on all objects.Prototype **Pollution vulnerability report**[https://snyk.io/test/npm/jquery/3.3.1](https://snyk.io/test/npm/jquery/3.3.1)
|Bootstrap 4.3.1|In Bootstrap before 3.4.1 and 4.3.x before 4.3.1, XSS is possible in the tooltip or popover data-template attribute.  *Integrity Impact Partial* (Modification of some system files or information is possible, but the attacker does not have control over what can be modified, or the scope of what the attacker can affect is limited.)Availability Impact None (There is no impact to the availability of the system.)  *Access Complexity Medium* (The access conditions are somewhat specialized. Some preconditions must be satistified to exploit)*Authentication Not required* (Authentication is not required to exploit the vulnerability.)**Gained Access None**  *Vulnerability Type(s) Cross Site Scripting*  *CWE ID 79*: [https://www.cvedetails.com/cve/CVE-2019-8331/](https://www.cvedetails.com/cve/CVE-2019-8331/)


| Test Environment setup | Description |
|--|--|
|Postman|Look at burp suite section to learn how to integrate Postman and burp suite. Overall, with burp suite, fairly easy to make the collections and run them. Easy enough to pass around the collections as json too, just gotta import and export.
| Burpsuite | As noted, burpsuite has postman integration and it is extremely simple. You click around with burp suite proxing your browser and then you can select the urls you want to export. After you have them selected you can right click and, with the postman extension downloaded, export as a postman json collection. You can then just pop into Postman and import the json. It is pretty easy to pass around the collections as json files.The website we are trying to pen test is and HTTPS server and that makes setting up burpsuite to work a little harder. We needed to download a CA cert for Burpsuite to work. Documentation from burpsuite [https://portswigger.net/support/installing-burp-suites-ca-certificate-in-chrome](https://portswigger.net/support/installing-burp-suites-ca-certificate-in-chrome) and [https://portswigger.net/support/installing-burp-suites-ca-certificate-in-internet-explorer](https://portswigger.net/support/installing-burp-suites-ca-certificate-in-internet-explorer). Overall you need to set up your proxy, go to [http://burp](http://burp/), download the CA cert, run the file and make sure to put it into root trusted certs (at least for chrome). After that everything worked |
|Fiddler|Found it fairly easy to setup and run will probably not use that much now that we have found the burp suite integration for postman making it much easier to work

|Screen Test|scripts|Results
|--|--|--|
| Specimen: Biological Profile | N/A |N/A
|Specimen: DNA|N/A|N/A
|Specimen: Isotope|N/A|N/A


