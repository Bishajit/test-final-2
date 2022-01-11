# pull ubuntu image
FROM ubuntu:latest

# update the current version
RUN apt update -y

# Install pip and others build tools
RUN apt install -y pip python-dev build-essential libssl-dev libffi-dev
# pull nginx image
FROM nginx:latest

RUN rm /etc/nginx/conf.d/default.conf
RUN ls /etc/nginx/conf.d

# create web.conf
COPY ./default.conf /etc/nginx/conf.d/default.conf
RUN ls /etc/nginx/conf.d

# check the configurations file format
RUN nginx -t

COPY ./frontend/ /usr/share/nginx/html/
