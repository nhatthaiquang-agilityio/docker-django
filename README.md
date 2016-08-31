# Docker django
Set up a Django application and development environment using Docker.

# Requirements:
+ [Install Docker](https://docs.docker.com/engine/installation/)
+ Ubuntu 14.04


# Run command:

+ Build docker:
	```
	$cd docker-django
	$ docker build -t nhatthai/myapp_django  .
	```

+ Run server:
	```
	$docker run --publish=8001:8000 nhatthai/myapp_django:latest
	```

+ Running some Django management commands on the Docker host
	```
	$docker run --rm -i -t --entrypoint=/bin/bash nhatthai/myapp_django:latest
	root@a94c8a5eed4a:/srv/myapp# ./manage.py createsuperuser
	```

+ Check django app:
	```
	http://localhost:8001
	```

# Reference:
+ [Django application into Docker container images](http://michal.karzynski.pl/blog/2015/04/19/packaging-django-applications-as-docker-container-images/)
+ [Getting started with Docker, Compose and Django](https://howchoo.com/g/y2y1mtkznda/getting-started-with-docker-compose-and-django)
