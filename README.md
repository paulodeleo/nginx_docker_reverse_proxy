A demo of how to setup nginx as a reverse proxy (single http entry point) to a second nginx server and an apache server.


To start all three containers run:

  `docker-compose up`

You should be able to open:

  http://localhost:8080

and see nginx's _"Welcome to nginx!"_ message.

And you should be able to open:

  http://localhost:8080/apache

and see apache's _"It works!"_ message.


This can serve as a basic example of how to setup a wordpress site on "/blog" of an existing nginx site (the leading `/` only on `http://docker-apache/` line of `nginx.conf` file is important for this to work).


Based on [this article](https://www.thepolyglotdeveloper.com/2017/03/nginx-reverse-proxy-containerized-docker-applications/) by THE POLYGLOT DEVELOPER and improved to use a subdirectory for apache.
