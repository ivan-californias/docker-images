NO_CACHE=false

all: build push

build:
	docker build --no-cache=${NO_CACHE} -t ivancalifornias/centos-7-robot-framework .

push:
	docker push ivancalifornias/centos-7-robot-framework

.PHONY: build push

