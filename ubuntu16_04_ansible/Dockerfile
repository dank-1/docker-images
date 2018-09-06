FROM ubuntu:16.04

RUN apt-get update && \
    apt-get install -y python-minimal python-pip && \
    apt-get install -y software-properties-common build-essential openssh-client && \
    pip install ansible boto boto3 awscli
