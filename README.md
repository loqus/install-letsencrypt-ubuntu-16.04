# install-letsencrypt-ubuntu-16.04
Install LetsEncrypt Ubuntu

sudo apt-get update

sudo apt-get install letsencrypt

Add a domain .conf file in NginX of Apache2 if needed

/etc/nginx/sites-available/ or /etc/apache2/sites-available/

cd /letsencrypt

Add Cert for www.domain.com

sudo ./letsencrypt-auto --server https://acme-v01.api.letsencrypt.org/directory -d www.domain.com -d domain.com

Add Cert for subdomain

sudo ./letsencrypt-auto --server https://acme-v01.api.letsencrypt.org/directory -d static.domain.com

Renew Cert:

sudo ./letsencrypt-auto renew --server https://acme-v01.api.letsencrypt.org/directory
