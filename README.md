# Dorkers
Dorks for Shodan and Google

## Shodan

`http.html:/dana-na/` - SSL VPN That is vulnerable with RCE CVE-2019-11510


`hacked-router-help-sos` - Hacked routers :-)


`NETSurveillance uc-httpd` - user:admin no passwords :-)


`IPC$ all storage devices` - Home routers' storage or attached USB Storage (Many with no PW)


`port:23 console gateway -password` - Open telnet no PW required


`"polycom command shell"` - Polycom Video conference system no-auth shell, most have open web config admin try for fun 


`NCR Port:"161"` - ATM's :-)


`HTTP/1.1 307 Temporary Redirect Location: /containers country:"US"` - Container Advisor dork


`html:"def_wirelesspassword"` - HTML tag looking for passwords in source

`country:xx http.status:200 http.component:odoo port:8069` - After finding instances go to /web/database/manager most of the time there is either no password or it's "admin"

`Model: PYNG-HUB Crestron` - IoT 
`x-jenkins 200` - Internet facing Jenkins servers, some unauthenticated.


### Useful for identifying installations


`http.status:200` - Useful for sorting search results

`html:` or `http.html:` - Search for HTML tags / code

`http.favicon.hash` - Search for hash of a specific favicon, very efficient to find fresh/basic installations of software.


## Google
`inurl:%3Dhttps%3A%2F%2F` - Open redirect/SSRF/Local File Disclosure


## Examples hunting for exploits

### Horde Webmail Dorks
`html:"horde_login"` - Shodan search for Horde webmail 


`inurl:/imp/login.php` - Google




## BinaryEdge.io
`http.body:dana-na ` - Find installations of Pulse VPN

`ssl.cert.subject.commonName:*vpn.*` - Find SSL certs with vpn in sub-domain name - Uses Asteriks(*) for wildcard.
