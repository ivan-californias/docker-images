FROM centos:7

RUN yum -y install epel-release && yum -y update && yum clean all

RUN mkdir -p /go && chmod -R 777 /go

RUN rpm --import https://mirror.go-repo.io/centos/RPM-GPG-KEY-GO-REPO && \
	curl -s https://mirror.go-repo.io/centos/go-repo.repo -o /etc/yum.repos.d/go-repo.repo

RUN yum -y install git golang make rpm-build sendemail && yum clean all

ENV GOPATH /go

WORKDIR /go
