FROM centos:7

RUN yum -y install epel-release && yum -y update && yum clean all

RUN yum -y install git gcc make rpm-build sendemail wget sudo vim xorg-x11-server-Xvfb xorg-x11-font* python python2-pip libxml2-python python-devel libxml2 libxml2-devel python36 python36-devel && yum clean all

RUN pip install --upgrade pip && pip install robotframework robotframework-selenium2library==1.8.0 robotframework-extendedselenium2library unidecode  robotframework-seleniumlibrary robotframework-xvfb boto3 elasticsearch requests requests-aws4auth

RUN python3.6 -m ensurepip && python3.6 -m pip install pytz mitmproxy

RUN wget https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm?authuser=0 -O /tmp/google-chrome.rpm && yum install -y /tmp/google-chrome.rpm && rm /tmp/google-chrome.rpm

RUN wget https://chromedriver.storage.googleapis.com/2.41/chromedriver_linux64.zip -O /tmp/chromedriver.zip && unzip /tmp/chromedriver.zip -d /bin && rm /tmp/chromedriver.zip

RUN yum -y install google-noto-emoji-fonts google-noto-fonts-common google-roboto-condensed-fonts google-roboto-fonts google-roboto-mono-fonts google-crosextra-caladea-fonts google-crosextra-carlito-fonts google-droid-sans-fonts google-droid-sans-mono-fonts google-droid-serif-fonts google-noto-sans-fonts google-noto-sans-ui-fonts google-noto-serif-fonts && yum clean all

# Create user robot
RUN useradd -m -d /robot -s /bin/bash robot
RUN usermod -aG wheel robot
RUN echo "robot ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
USER robot
WORKDIR /robot


