# Dorks are cool
### Dorks for Google, Shodan and BinaryEdge
Only for use on bug bounty programs or in cordination with a legal security assesment.

I am in no way responsible for the usage of these search queries.

Be responsible thanks - https://www.bugcrowd.com/resource/what-is-responsible-disclosure/


This repository is *"under construction"* feel free to make pull requests :-)


## Web services

*Example of how to fingerprint services with the different search engines:*

Service |Google | Shodan | BinaryEdge | CVE/Exploit
--- | --- | --- | --- | ---
*Pulse VPN (RCE VULN)* | ``inurl:"/dana-na/"`` | ``http.html:/dana-na/`` | ``http.body:dana-na`` | *CVE-2019-11510*
*Horde Webamil (RCE VULN)*| ``inurl:/imp/login.php`` | ``html:"horde_login"`` | ``http.body:horde_login`` | *CVE 2018-19518*


*NOTE:* Some services have already been fingerprinted by Shodan and BinaryEdge and you can use the `product:` tag

**Examples:**

*BinaryEdge* - `product:"Pulse Secure VPN gateway http config"`

*Shodan* - `product:"Pulse Secure"`


## Random dorks


### Google
`inurl:%3Dhttps%3A%2F%2F` - Open redirect/SSRF/Local File Disclosure

*Read ahrefs blog post to see all search operators for Google - https://ahrefs.com/blog/google-advanced-search-operators/*

### Shodan.io

*Some of these dorks are old as fuck just FYI :-)*

`hacked-router-help-sos` - Hacked routers :D

`NETSurveillance uc-httpd` - user:admin no passwords most likely

`IPC$ all storage devices` - Home routers' storage or attached USB Storage (Many with no PW)

`port:23 console gateway -password` - Open telnet no PW required

`"polycom command shell"` - Polycom Video conference system no-auth shell, most have open web config admin try for fun 

`NCR Port:"161"` - ATM's :-)

`HTTP/1.1 307 Temporary Redirect Location: /containers country:"US"` - Container Advisor dork

`html:"def_wirelesspassword"` - HTML tag looking for passwords in source of brazillian routers

`country:xx http.status:200 http.component:odoo port:8069` - After finding instances go to /web/database/manager most of the time there is either no password or it's "admin"

`Model: PYNG-HUB Crestron` - IoT 

`x-jenkins 200` - Internet facing Jenkins servers, some unauthenticated. :O


*Read the full list of filters for Shodan here - https://beta.shodan.io/search/filters*

### BinaryEdge.io


`ssl.cert.subject.commonName:*vpn.*` - Find SSL certs with vpn in sub-domain name - Uses Asteriks(*) for wildcard.

`Fortinet security device httpd` - Finds fortinet SSL VPN installations - Some vulnerable to CVE-2018-13379

`product:"Exim smtpd" version:<4.92` - Finds vulnerable Exim smtp servers - Vulnerable to multiple CVE's but mainly CVE-2019-15846

*Read the search Docs to find even more tags to use! - https://docs.binaryedge.io/search/*




### SQL Injection Google Dorks

Some of these are probably shit and require tuning with other tags / dorks, experiment with them. :D


```SQL
intext:"error in your SQL syntax"
intext:"mysql_num_rows()" 
in****:"mysql_fetch_array()" 
in****:"Error Occurred While Processing Request" 
in****:"Server Error in '/' Application" 
in****:"Microsoft OLE DB Provider for ODBC Drivers error" 
in****:"InvalidQuerystring" 
in****:"OLE DB Provider for ODBC" 
in****:"VBScript Runtime" 
in****:"ADODB.Field" 
in****:"BOF or EOF" 
in****:"ADODB.Command" 
in****:"JET Database" 
in****:"mysql_fetch_row()" 
in****:"Syntax error" 
in****:"include()" 
in****:"mysql_fetch_assoc()" 
in****:"mysql_fetch_object()" 
in****:"mysql_numrows()" 
in****:"GetArray()" 
in****:"FetchRow()" 
in****:"Input string was not in a correct format" 
inurl:/id= intext:"You have an error in your SQL syntax" 
inurl:&#8221;main.php?t=
inurl:&#8221;games.php?id=
inurl:&#8221;guide.php?id=
inurl:&#8221;index.php?cat=
allinurl:&#8221;review.php?sid=
inurl:&#8221;index2.php?id=
inurl:&#8221;main.php?id=
inurl:zoom.php?id=site:.il
inurl:&#8221;details.php?id=
inurl:&#8221;?came=
inurl:&#8221;index.php?page=
inurl:&#8221;home.php?cat=
inurl:&#8221;index2.php?id=
```
