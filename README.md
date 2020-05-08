# Traefik 1.7.24 
Traefik 1.7.24 usado na estrutura Brasil IP.
 
 # Docker Run
 ```
docker run -d \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v $PWD/traefik.toml:/traefik.toml \
  -v $PWD/acme.json:/acme.json \
  -p 80:80 \
  -p 443:443 \
  -l traefik.frontend.rule=Host:monitor.brasil-ip.net \
  -l traefik.port=8080 \
  --network web \
  --name traefik \
  traefik:1.7.24
  ```
