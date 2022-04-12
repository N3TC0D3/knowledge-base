# Linux 🐧
## Certbot
### Certificate paths
When certificates are successfully deployed, they can be located at the following path: `/etc/letsencrypt/live/<domain-name>`
In some cases there might be a numeric appendix, usually a 4-letter number like "0001"

### Wildcard certificate
Wildcard certificates in certbot must be deployed manually since they require a DNS-TXT record to be set. The setup process can be initiated using the following command:
`certbot certonly --manual --preferred-challenges=dns --email benmihm@netcode.dev --server https://acme-v02.api.letsencrypt.org/directory --agree-tos -d *.netcode.dev -d netcode.dev`
Of course you have to replace your email address and domain names accordingly

### DNS records
If you choose to validate your authorization to optain a certificate for a given domain through DNS you must add a TXT-record in your DNS settings. 
You should check if your record has been updated using e.g. https://mxtoolbox.com/. Just enter `_acme-challenge.<your-domain>` into the search field you should find a list of records including the TXT record, if updated already