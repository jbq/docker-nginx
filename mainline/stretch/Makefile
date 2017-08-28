IMAGE = jbquenot/nginx:$(shell awk '$$1 == "ENV" && $$2 == "NGINX_VERSION" { print $$3; exit }' < Dockerfile | sed -e 's/-.*$$//')

all: build push

build:
	docker build -t $(IMAGE) .

push:
	docker push $(IMAGE)
