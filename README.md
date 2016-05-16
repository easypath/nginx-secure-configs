# Secure NGINX configs
A repository of virtual-host configuration templates for use with NGINX, pre-configued for security. All templates score A+ on [Qualys SSL Labs](https://www.ssllabs.com/ssltest/).

### Browser/client support
The templates only support modern clients and browsers. Legacy clients, including Internet Explorer 9 or below on Windows XP, are **not** supported. To modify legacy-client support, tweak the SSL cipher list (see [here for more info](https://cipherli.st/)).

### Requirements
* NGINX, tested on version 1.10.0 (Ubuntu)
* SSL certificate

### Template notes
#### WordPress:
* Requires PHP7.0 FPM
* Tested with WordPress 4.5.2

#### CloudFlare:
* Requires a free or paid account
* CloudFlare can also redirect HTTP to HTTPS using a page rule, however in testing this seemed to cause chained 301 redirects - i.e. http://example.com to https://example.com to https://www.example.com
* SEO best-practice is to do a "Class B" redirect, i.e. redirect "bare" domains - without "www" - to www.example.com (see [here](https://blog.codingoutloud.com/2010/07/26/4-reasons-to-embrace-the-www-subdomain-prefix-in-your-web-addresses-and-how-to-do-it-right/) for more info)
* Pre-configured to restore the visitor's original IP; the list of CloudFlare IP addresses must be periodically updated (see [here](https://support.cloudflare.com/hc/en-us/articles/200170706-How-do-I-restore-original-visitor-IP-with-Nginx-) for more info)

### Credits
The template is based on the following resources:
* [Mozilla SSL Configuration Generator](https://mozilla.github.io/server-side-tls/ssl-config-generator/)
* [Cipherli.st](https://cipherli.st/)
* [Bjørn Johansen](https://bjornjohansen.no/optimizing-https-nginx)
* [Julian Simioni](https://juliansimioni.com/blog/https-on-nginx-from-zero-to-a-plus-part-2-configuration-ciphersuites-and-performance/)
