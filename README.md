A demo of how to setup nginx as a reverse proxy (single http entry point) to a second nginx server and an apache server.


To build the custom `reverseproxy` image run:

  `docker build -t reverseproxy .`

Then start all three containers using:

  `docker-compose up`

You should be able to open:

  http://localhost:8080

and see nginx's "Welcome to nginx!" message.

And you should be able to open:

  http://localhost:8080/apache

and see apache's "It works!" message.


This can serve as a basic example of how to setup a wordpress site on "/blog" of an existing nginx site (the leading `/` only on `http://docker-apache/` line of `nginx.conf` file is important for this to work).


Based on [this article](https://www.thepolyglotdeveloper.com/2017/03/nginx-reverse-proxy-containerized-docker-applications/) by THE POLYGLOT DEVELOPER and improved to use a subdirectory for apache.
