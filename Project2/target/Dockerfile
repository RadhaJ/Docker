# Pull base image
From tomcat:8-jre8

# Maintainer
MAINTAINER "Radha Jarubula <jarubura@mail.uc.edu">

# Configure apache
RUN a2enmod rewrite
RUN chown -R www-data:www-data /var/www
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

EXPOSE 80

# Copy to images tomcat path
ADD Project2.war /usr/local/tomcat/webapps/
