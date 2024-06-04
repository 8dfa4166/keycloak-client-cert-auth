FROM nginx:latest

COPY conf/default.conf /etc/nginx/conf.d/default.conf
COPY ssl/server.pem /etc/nginx/conf.d/server.pem
COPY ssl/server.key /etc/nginx/conf.d/server.key
COPY ssl/rootCA2.pem /etc/nginx/conf.d/rootCA2.pem
COPY ssl/inCA2.pem /etc/nginx/conf.d/inCA2.pem
RUN cat /etc/nginx/conf.d/rootCA2.pem /etc/nginx/conf.d/inCA2.pem > /etc/nginx/conf.d/client.pem