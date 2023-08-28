FROM amazon/aws-cli

RUN yum update -y && yum install -y shadow-utils && yum clean all

RUN groupadd -g 1000 aws \
  && useradd -u 1000 -g 1000 -s /bin/bash -m -d /home/aws aws

WORKDIR /home/aws