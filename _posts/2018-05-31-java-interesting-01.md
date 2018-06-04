---
title: "Interesting libraries at sight - 01"
comments: true
tags:
  - java
---

Taking note of some interesting libraries mentioned in Awesome Java Newsletter Issue 107

<!--more-->

### Security

Alternatives if Spring Security is not your cup of tea:

* [jCasbin](https://github.com/casbin/casbin) - An authorization library that supports access control models like ACL, RBAC, ABAC in Java

which reminds me of 

* [OACC](http://oaccframework.org/) - Java Application Security Framework. 

### Logging

* [Logbook](https://github.com/zalando/logbook) - An extensible Java library for HTTP request and response logging. Worth taking note on this point: 
Logbook puts a big emphasis on logging the actual request/response body that was sent over the wire. The Apache HttpClient, among the following alternatives, 
is the only technology to support that.
