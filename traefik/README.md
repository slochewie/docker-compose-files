docker run -d -p 8082:8080 -p 82:80 \
-v $PWD/traefik.yml:/etc/traefik/traefik.yml \
-v /var/run/docker.sock:/var/run/docker.sock \
--name traefik \
traefik:v2.0