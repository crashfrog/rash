rash
====

RASh - the RESTful API Shell.

Purpose
-------

RESTful API's are all over the place, but somewhat hard to explore - even though self-description and explorability lie at the heart of a good RESTful API. The RASh aims to be a useful tool for playing around with third-party API's, which is frequently easier than just reading documentation.

Philosophy
----------

URI's are hierarchial, and programmers know how to interact with shells and explore filesystems. Exploring a web API should feel like exploring a filesystem.

Usage
-----

Usage should feel like:

```
$ rash http://www.example.com/api/
RASh 1.0.1 - the RESTful API Shell.
*GET api/*
*GET api/*cd resources/
*GET api/resources* ls
api/resources  POST,GET,PUT,DELETE --
api/resources/response JSON    1.2k
api/resources/query    POST    --
api/resources/status   GET --
api/resources/object1  GET,DELETE --
api/resources/object2  GET --
*GET api/resources* cd response/
*GET api/resources/response* ls
{"ApiVersion":"1.0",
"HttpMode":"GET",
"Resources":[
  {"ObjectName":"object1",
  "ObjectContent":"apple",
  "ObjectUri":"http://www.example.com/api/resources/object1},
  {"ObjectName":"object2",
  "ObjectContent":"banana",
  "ObjectUri":"http://www.example.com/api/resources/object2}
]}
```
