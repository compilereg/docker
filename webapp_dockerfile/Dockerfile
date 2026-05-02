FROM ubuntu:latest
LABEL maintainer=compiler@aast.edu
ENV DEBIAN_FRONTEND=noninteractive
RUN apt update
RUN apt install apache2 –y
RUN echo "Welcome to  my Webserver" > /var/www/html/index.html
CMD ["/usr/sbin/apache2ctl", "-DFOREGROUND"]

