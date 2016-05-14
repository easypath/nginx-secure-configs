# Secure NGINX config for WordPress
Virtual-host configuration template with customizations for WordPress. Scores A+ on [Qualys SSL Labs](https://www.ssllabs.com/ssltest/analyze.html?d=easypath.ca).

## Browser/client support
This configuration only supports modern clients and browsers. Legacy clients, including Internet Explorer 9 or below on Windows XP, are **not** supported. To modify legacy-client support, tweak the SSL cipher list (see [here for more info](https://cipherli.st/)).

## Requirements
* NGINX, tested on version 1.10.0 (Ubuntu)
* PHP7.0 FPM
* SSL certificate

## Credits
The template is based on the following resources:
* [Mozilla SSL Configuration Generator](https://mozilla.github.io/server-side-tls/ssl-config-generator/)
* [Cipherli.st](https://cipherli.st/)
* [Bjørn Johansen](https://bjornjohansen.no/optimizing-https-nginx)
* [Julian Simioni](https://juliansimioni.com/blog/https-on-nginx-from-zero-to-a-plus-part-2-configuration-ciphersuites-and-performance/)
