FROM nginx:1.10

# Add start script
ADD .docker/services/webserver/config/start.sh /
RUN chmod +x start.sh

# Add nginx config file
ADD .docker/services/webserver/config/nginx.tmpl /

# Add SSL certs to location specified in nginx.conf
ADD .docker/services/webserver/config/*.crt /etc/ssl/certs/
ADD .docker/services/webserver/config/*.key /etc/ssl/private/

# Execute start script
CMD ["./start.sh"]
