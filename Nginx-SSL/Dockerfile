FROM gilangvperdana/ssl:nginx

WORKDIR /var/www/html/

COPY ./HTML/ /var/www/html/

EXPOSE 80

STOPSIGNAL SIGTERM

CMD ["nginx", "-g", "daemon off;"]

