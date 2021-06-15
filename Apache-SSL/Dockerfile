FROM gilangvperdana/ssl:apache2

WORKDIR /var/www/html/

COPY ./HTML/ /var/www/html/

EXPOSE 80
EXPOSE 443

STOPSIGNAL SIGTERM

CMD ["apachectl", "-D", "FOREGROUND"]
