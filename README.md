# M_HeadscaleServer
Docker-compose to run the headscale server, reachable at the address `https://headscale.{my.domain}`, and the headscale web page for administration, reachable at the address `https://admin.headscale.{my.domain}`.

## Install
A Caddy container operates as reverse proxy to redirect the requests to the server. It's just required to specify `my.domain` through the variable `SITE_DOMAIN` into the environment file `.env`, like
```
# CADDY
SITE_DOMAIN="example.com"
```
To test it, run
```
docker compose up -d
```
and open web page at the address 
```
https://admin.headscale.example.com
```
