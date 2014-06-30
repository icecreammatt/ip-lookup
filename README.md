ip-lookup
=========

NodeJS application which responds with the clients IP address

Sample Nginx Config

```
server {
    listen  80;
    server_name ip.domain.com;
    location / {
        proxy_pass          http://localhost:3002/;
        proxy_redirect off;
        proxy_set_header Host $host;
        proxy_set_header X-RealIP $remote_addr;
    }
}
```
