FROM alpine:latest

LABEL org.opencontainers.image.authors="rmontemayor@mac.com"
LABEL org.opencontainers.image.source=https://github.com/jduncan-rva/container-fundamentals
LABEL org.opencontainers.image.description="Containter Fundamentals - Static Website Image"
LABEL org.opencontainers.image.licenses=APACHE2
LABEL org.openconatiners.image.server_type="edge_server"

RUN apk update
RUN apk add nginx --purge

COPY config/nginx.conf /etc/nginx/
COPY web_content/ /var/www
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
