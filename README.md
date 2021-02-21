# Personal notifications

I recommend to clone this repo and create an own image for having an actual nginx-image  

Create an own image

```
cd <directory with Dockerfile>
docker build -t autoindex .
```

# Nginx AutoIndex

[![](https://images.microbadger.com/badges/version/jorgeandrada/nginx-autoindex.svg)](https://microbadger.com/images/jorgeandrada/nginx-autoindex "Get your own version badge on microbadger.com") [![](https://images.microbadger.com/badges/image/jorgeandrada/nginx-autoindex.svg)](https://microbadger.com/images/jorgeandrada/nginx-autoindex "Get your own image badge on microbadger.com")

A branch of nginx:latest with autoindex on.
Serves all files in `/usr/share/nginx/html`

#### nginx:latest

    location / {
        root   /usr/share/nginx/html;
        index  index.html index.htm;
    }


#### jorgeandrada/nginx-autoindex:latest

    location / {
        root   /usr/share/nginx/html;
        autoindex on;
    }

```
docker run --name=web -p 80:80  -h web -v path_web_site:/usr/share/nginx/html -d jorgeandrada/nginx-autoindex
```

