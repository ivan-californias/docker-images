FROM centos:7

RUN curl -sL https://rpm.nodesource.com/setup_10.x | bash -

RUN yum -y install epel-release && yum -y update && yum clean all

RUN yum -y install git nodejs make rpm-build sendemail && yum clean all


