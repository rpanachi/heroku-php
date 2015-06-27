heroku-php
===============

Heroku PHP container built from its buildpack using tutum/buildstep

Usage
-----

Create a `Dockerfile` similar to the following in your application code folder:

```Dockerfile
FROM rpanachi/heroku-php
ADD . /app
EXPOSE 3000
CMD vendor/bin/heroku-php-apache2
```

Modify the `EXPOSE` and `CMD` directives with the port to be exposed and the command
used to launch your application respectively.

Then, execute the following to build the image:

	docker build -t myuser/myapp .

This will create an image named `myuser/myapp` with your application ready to go.
To launch it, just type:

	docker run -p 3000 myuser/myapp

That's it!
