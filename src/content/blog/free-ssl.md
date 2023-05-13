---
title: "FREE SSL certificate for your website!"
pubDate: "Feb 14, 2018"
heroImage: "https://images.unsplash.com/photo-1633265486064-086b219458ec?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"
---

### Guide

Ok so I’m going to show you how to get your first ssl certificate for FREE! yup, you read right for FREE just follow up these simple steps.

1. go to this website letsencrypt.com and there’s a list of clients to generate your ssl certificate, even web base apps.
2. I’ll show you how to generate your ssl with this site, zerossl.com
3. Click on “online tools”
4. Click on “start” on the “Free certificate wizard”
5. choose “http”, write your domain, read and accept the TOS.
6. So it will generate the csr … click the download button to download your csr, then click next and it will generate the key
7. Final step, you need to serve that respond in the endpoint provided
8. DONE!! download the .crt and .key !

### Basic use of ssl certs in nginx

```
server {
 listen 443 ssl;
 server_name example.com;
 ssl_certificate_key /certs/example.com.key;
 ssl_certificate /certs/example.com.crt;
 ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
}
server {
  listen 80;
  server_name example.com;
  return 301 https://$host$request_uri;
}
```

#### [Also in medium](https://medium.com/@g3org3dev/free-ssl-certs-15fa31303770)
