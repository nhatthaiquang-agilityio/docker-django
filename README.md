# Docker django
Set up a Django application and development environment using Docker.

# Requirements:
--------------
+[Install Docker](https://docs.docker.com/engine/installation/)
+ Ubuntu 14.04


# Run command:
--------------
+ Build docker:
	```
	$cd docker-django
	$ docker build -t nhatthai/myapp_django  .
	```

+ Run server:
	```
	$docker run --publish=8001:8000 nhatthai/myapp_django:latest
	```

+ Check django app:
	```
	http://localhost:8001
	```

# Reference:
-----------
+ [Django application into Docker container images](http://michal.karzynski.pl/blog/2015/04/19/packaging-django-applications-as-docker-container-images/)
+ [Getting started with Docker, Compose and Django](https://howchoo.com/g/y2y1mtkznda/getting-started-with-docker-compose-and-django)
