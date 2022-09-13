# Nginx-hello-world

Create a docker network:
```sh
docker network create --driver bridge node
```

Up some nginx's servers to test the Nginx load balance:
```sh
docker run -d --name node1 --network node nginx
```
```sh
docker run -d --name node2 --network node nginx
```
```sh
docker run -d --name node3 --network node nginx
```

Up a main nginx server:
```sh
docker run --rm -it -v $(pwd)/nginx/nginx.conf:/etc/nginx/nginx.conf -v $(pwd)/html:/usr/share/nginx/html --network node -p 8080:80 nginx
```
