IMAGE := ivancalifornias/generic-builder

all: build push

build:
	docker build -t ${IMAGE} .

push:
	docker push ${IMAGE}

.PHONY: build push

