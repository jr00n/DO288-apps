FROM docker.io/nginx:latest
RUN find / -type d -exec chgrp root {} \; && \
  find / -type d -exec chmod g+w {} \; && \ 
  sed -i '/user[[:space:]]*nginx;/d' /etc/nginx/nginx.conf && \ 
  sed -i 's/listen[[:space:]]*.*/listen 8080;/' /etc/nginx/conf.d/default.conf

LABEL io.openshift.expose-services "8080/tcp:http"
EXPOSE 8080
USER 1001
