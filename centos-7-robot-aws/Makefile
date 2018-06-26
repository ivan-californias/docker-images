NO_CACHE=false
IMAGE_NAME=centos-7-robot-aws

all: build push

build:
	docker build --no-cache=${NO_CACHE} -t ivancalifornias/${IMAGE_NAME} .

push:
	docker push ivancalifornias/${IMAGE_NAME}

.PHONY: build push

