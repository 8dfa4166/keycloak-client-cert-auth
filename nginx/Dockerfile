FROM nginx:latest

COPY conf/default.conf /etc/nginx/conf.d/default.conf
COPY ssl/server.pem /etc/nginx/conf.d/server.pem
COPY ssl/server.key /etc/nginx/conf.d/server.key
COPY ssl/rootCA2.pem /etc/nginx/conf.d/client.pem