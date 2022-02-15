Create/login account in [DuckDNS](https://www.duckdns.org) and copy the token from your domain.

Download the repository
```
git clone https://github.com/AzagraMac/GenCertLetsencrypt.git
```

we edit the parameters of our domain and e-mail.
```
- URL=YOUR_DOMAIN.duckdns.org
- DUCKDNSTOKEN=YOUR_TOKEN
- EMAIL="YOUR_MAIL"
```

We deploy the docker container
```
docker-compose up -d
```


```
$ ls -l /root/docker/letsencrypt/config/etc/letsencrypt/archive/YOUR_DOMAIN.duckdns.org/
total 20
-rw-r--r-- 1 root root 2208 feb 15 11:13 certX.pem
-rw-r--r-- 1 root root 3749 feb 15 11:13 chainX.pem
-rw-r--r-- 1 root root 5957 feb 15 11:13 fullchainX.pem
-rw------- 1 root root 3272 feb 15 11:13 privkeyX.pem
```
We will have the certificate with its private key and the intermediate certificate, we will choose file, where X is the highest file number we have, the previous ones are not deleted.
