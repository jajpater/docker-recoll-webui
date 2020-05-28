# docker-recoll-webui
recoll with webui in a docker container

- used python3 and new updated recoll-web-ui https://framagit.org/medoc92/recollwebui/ version
- creates a python standalone recoll server inside a docker container listening on port 8080 mapped on port 9090
- to start indexing run this command on your system:
    `docker exec CONTAINER_ID recollindex` or use recollindex.sh
- change `CONTAINER_ID` and paths to your needs
- settings for recoll are stored in `/root/.recoll/recoll.conf`
- the path of what will be indexed is `/docs`

# links
- stolen from: https://github.com/dsheyp/docker-recoll-webui
- source project: https://github.com/amsaravi/docker-recoll-webui
- docker hub: https://hub.docker.com/repository/docker/amsaravi/recoll-web-ui
# installation steps

do: 
clone repro
adjust docker-compose.yml to your whishes 
docker-compose build
docker-compose up -d

- for simplicity there is no user level configuration. you can maintain your container and change configs in `/root/.recoll/recoll.conf` and use docker exec command (not run command) to rebuild index
