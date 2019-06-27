# Dorkers
Dorks for Shodan and Google

## Shodan
`hacked-router-help-sos` - Hacked routers :-)


`NETSurveillance uc-httpd` - user:admin no passwords :-)


`IPC$ all storage devices` - Home routers' storage or attached USB Storage (Many with no PW)


`port:23 console gateway -password` - Open telnet no PW required


`"polycom command shell"` - Polycom Video conference system no-auth shell, most have open web config admin try for fun 

`NCR Port:"161"` - ATM's :-)

### Useful for identifying installations
`html:` - Search for HTML tags / code

`http.favicon.hash` - Search for hash of a specific favicon, very efficient to find fresh/basic installations of software.


## Google
`inurl:%3Dhttps%3A%2F%2F` - Open redirect/SSRF/Local File Disclosure


## Examples hunting for exploits

### Horde Webmail Dorks
`html:"horde_login"` - Shodan search for Horde webmail 


`inurl:/imp/login.php` - Google


