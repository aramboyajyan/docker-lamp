FROM httpd:2.4.41
#FROM debian:stretch
RUN apt-get update && apt-get install -y
# Enable mod_rewrite.
#RUN a2enmod rewrite
#RUN sed -i '/LoadModule rewrite_module/s/^#//g' /usr/local/apache2/conf/httpd.conf && \
#    sed -i 's#AllowOverride [Nn]one#AllowOverride All#' /usr/local/apache2/conf/httpd.conf
# Copy apache vhost file to proxy php requests to php-fpm container
COPY apache.conf /usr/local/apache2/conf/apache.conf
RUN echo "Include /usr/local/apache2/conf/apache.conf" \
    >> /usr/local/apache2/conf/httpd.conf
# Update permissions.
#RUN chown www-data:www-data /var/www/html/
