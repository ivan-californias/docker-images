FROM centos:7

RUN yum -y install epel-release && yum -y update && yum clean all

RUN yum -y install git make rpm-build sendemail wget && yum clean all

RUN yum -y install python python2-pip && yum clean all

RUN wget https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm?authuser=0 -O /tmp/google-chrome.rpm && yum install -y /tmp/google-chrome.rpm && rm /tmp/google-chrome.rpm && yum clean all

RUN wget https://chromedriver.storage.googleapis.com/2.38/chromedriver_linux64.zip -O /tmp/chromedriver.zip && unzip /tmp/chromedriver.zip -d /bin && rm /tmp/chromedriver.zip

RUN pip install --upgrade pip

RUN pip install robotframework robotframework-selenium2library==1.8.0 robotframework-extendedselenium2library unidecode



