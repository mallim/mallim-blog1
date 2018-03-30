---
title: "Let my future be Complete..."
comments: true
tags:
  - java
  - CompletableFuture
---

I have tried and put up some examples at https://github.com/mallim/java101 (look for completablefuture package).

On my laptop, RealLifeWithoutCompletableFutureExample took 15087 ms and RealLifeCompletableFutureExample 5098 ms.

Hmm.. so there is a a difference.

<!--more-->

### Libraries related to CompletableFuture 

* [tascalate-concurrent]{https://github.com/vsilaev/tascalate-concurrent]

### Libraries related to Executor

* [async-retry](https://github.com/nurkiewicz/async-retry)
* [vmlens Executor service](https://github.com/vmlens/executor-service) - A high throughput java executor service

### Parallel Stream --> CompletableFuture

* [Java 8: CompletableFuture vs Parallel Stream](http://fahdshariff.blogspot.sg/2016/06/java-8-completablefuture-vs-parallel.html?m=1)
* [Gentle introduction to Completable Future](https://blog.cngroup.dk/2015/08/04/completable-future/ ) gives a Thread Pool Size Formula

```
Nthreads) = Ncpu * Ucpu * (1 + W/C)

Ncpu - number of cpus
Ucpu - cpu utilization
W/C - ration of wait to compute time
```
