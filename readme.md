# Mern Todo-Apps with Docker

## Containers

* `client` with React on `https://localhost:3000` route
* `server` with Express on `https://localhost:5000` route
* `mongo` with MongoDB



## Usage

You can use `docker-compose up -d` command to deploy the container, or for every container separately, you can use `docker-compose up -d [container_name] client server adminmongo`

Get in to container and install more dependecies with `docker exec -it server /bin/sh` or `docker exec -it client /bin/sh` and then `npm install whatewer`.

Get logs from container to check everything is running correctly with `docker logs --tail 50 server` or `docker logs --tail 50 client`

Shut down containers with `docker-compose down`.

If you change `Dockerfile` rebuild container with `docker-compose build server`. Container names are `client`, `server`, `mongo` and `adminmongo`.

Access React app on `http://localhost:3000` and test the server on `https://localhost:5000/`.



## Additional notes

Tested on Linux Mint 20.1 / Ubuntu 20.04. 
