# How I explained REST to my brother

## Who is Roy Fielding?

Roy T. Fielding, Senior Principal Scientist at Adobe, is known for his pioneering work on the World Wide Web, open source, and software architecture. He wrote the standards for HTTP/1.x and URI, has been a contributor to many other Web technologies, and defined the REST architectural style. Dr. Fielding is a founder of the Apache HTTP Server Project, Chairman of the Apache Software Foundation, member of the ASF board of directors, and author of the Apache License 2.0. He has been honored with the ACM Software System Award, ACM SIGSOFT Impact Paper Award, OSCON 2000 Appaloosa Award for Vision, ICSE Most Influential Paper, and MIT Technology Review's first TR100. Dr. Fielding received his Ph.D. in Information and Computer Science from the University of California, Irvine.

## Why don’t the techniques that we use today work well when we need to be able to talk to all of the machines in the world?

 Because they weren't designed to be used like that. When Fielding and his colleagues started building the web, being able to talk to any machine anywhere in the world was a primary concern. But most of the techniques developers later used to get computers to talk to each other didn't have those requirements. You just needed to talk to a small group of machines.

## What is the HTTP protocol that Fielding and his friends created?

Hypertext Transfer Protocol (HTTP) is an application-layer protocol for transmitting hypermedia documents, such as HTML. It was designed for communication between web browsers and web servers, but it can also be used for other purposes. HTTP follows a classical client-server model, with a client opening a connection to make a request, then waiting until it receives a response. HTTP is a stateless protocol, meaning that the server does not keep any data (state) between two requests.

## What does a GET do?

GET is used to request data from a specified resource.
GET is one of the most common HTTP methods.

### Some other notes on GET requests

- GET requests can be cached
- GET requests remain in the browser history
- GET requests can be bookmarked
- GET requests should never be used when dealing with sensitive data
- GET requests have length restrictions
- GET requests are only used to request data (not modify)

## What does a POST do?

POST is used to send data to a server to create/update a resource.

POST is one of the most common HTTP methods.

### Some other notes on POST requests

- POST requests are never cached
- POST requests do not remain in the browser history
- POST requests cannot be bookmarked
- POST requests have no restrictions on data length

## What does PUT do?

 PUT is used to send data to a server to create/update a resource.

The difference between POST and PUT is that PUT requests are idempotent. That is, calling the same PUT request multiple times will always produce the same result. In contrast, calling a POST request repeatedly have side effects of creating the same resource multiple times.

## What does PATCH do?

The transdermal contraceptive patch is a safe and convenient birth control method that works really well if you always use it correctly. You wear the patch on certain parts of your body, and it releases hormones through your skin that prevent pregnancy. The patch has lots of other health benefits, too.
