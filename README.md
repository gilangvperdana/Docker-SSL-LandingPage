# Simply Deploy landingpage with SSL on Docker
    Simply deploy an SSL Landingpage with Nginx/Apache
```Environment:
Environment:
    1. VPS with Public IP and DNS Record Configured (CNAME & A).
    2. Linux Ubuntu Server.
    3. Docker.
```

# with Nginx
```
If you want to deploy your landing page with Nginx, goes to "Nginx-SSL" directory.
$ cd Nginx-SSL

don't forget to change the HTML file to be deployed, the contents of the HTML file to be deployed in the "HTML" folder.
after the HTML to be deployed is filled in, please create an image and run the image.
$ docker build -t yourimagename .
$ docker run -d -p 80:80 -p 443:443 your_image_name
```

# with Apache
```
If you want to deploy your landing page with Apache, goes to "Apache-SSL" directory.
$ cd Apache-SSL

Don't forget to change the HTML file to be deployed, the contents of the HTML file to be deployed in the "HTML" folder.
After the HTML to be deployed is filled in, please create an image and run the image.
$ docker build -t yourimagename .
$ docker run -d -p 80:80 -p 443:443 your_image_name
```

# Generate SSL Certificate
```
to get an https connection, after you run your new image, please enter to the container and generate a new certificate with the help of certbot.
$ docker ps (check your running container id)
$ docker exec -it container_id bash

for nginx:
$ certbot --nginx -d domain.com -d www.domain.com

for apache:
$ certbot --apache
```

# Access on
```
https://localhost or https://your.domain
```

# My DockerHub image:
```
https://hub.docker.com/r/gilangvperdana/ssl
```
