# Dorkers
Dorks for Shodan and Google

## Shodan
`html:` - Search for HTML tags / code
`http.favicon.hash` - Search for hash of a specific favicon, very efficient to find fresh/basic installations of software.


## Google
`inurl:%3Dhttps%3A%2F%2F` - Open redirect/SSRF/Local File Disclosure


## Examples hunting for exploits

### Horde Webmail Dorks
`html:"horde_login"` - Shodan search for Horde webmail 
`inurl:/imp/login.php` - Google
