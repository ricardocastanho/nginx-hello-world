# Nginx-hello-world

Up a nginx server:
```sh
docker run --rm -it -v $(pwd)/nginx/nginx.conf:/etc/nginx/nginx.conf -v $(pwd)/html:/usr/share/nginx/html -p 8080:80 nginx bash
```
