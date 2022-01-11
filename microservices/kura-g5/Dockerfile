#pull ubuntu image
FROM ubuntu:latest

#Pull python image
FROM python:latest

#update the current version
RUN apt update -y

#Install pip and others build tools
RUN apt install -y pip python-dev build-essential libssl-dev libffi-dev

#Make directory kura-g5
RUN mkdir /kura-g5

#Copy all files from kura-g5
COPY . /kura-g5

#make Working directory kura-g5
WORKDIR /kura-g5

#upgrade pip
RUN pip install --upgrade pip

#Install required libraries
RUN pip install -r requirements.txt

#Expose port
EXPOSE 5000
