FROM ubuntu:23.10
LABEL Description="A2C Docker Image"
RUN apt-get update && apt-get install curl -y
RUN curl -o AWSApp2Container-installer-linux.tar.gz https://app2container-release-us-east-1.s3.us-east-1.amazonaws.com/latest/linux/AWSApp2Container-installer-linux.tar.gz \
    && tar xvf AWSApp2Container-installer-linux.tar.gz
RUN ls \
    && sh install.sh
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
    && apt-get install unzip \
    && unzip awscliv2.zip \
    && ./aws/install
#CMD ["aws --version"]