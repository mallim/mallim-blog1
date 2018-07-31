---
title: "Learning Monos and Fluxes"
comments: true
tags:
  - reactor
  - flux
  - mono
---

This article's name was inspired by [101 Reactive Gems](https://github.com/reactor/reactive-streams-commons/issues/21)

<!--more-->

### Gem #1 - defer a Flux's blocking method 

Got the idea from [Developing Reactive applications with Reactive Streams and Java 8 by Brian Clozel, Sébastien Deleuze ](https://youtu.be/Cj4foJzPF80)

````java
Flux.defer( () -> Flux.iteratable( BlockRepository.findAllUsers() ) ).subscribeOn( Scheduler.elastic() )
````

### Gem #2 - publishOn and then eg to save user

Got the idea from [Developing Reactive applications with Reactive Streams and Java 8 by Brian Clozel, Sébastien Deleuze ](https://youtu.be/Cj4foJzPF80)

````java
Flux.publishOn( Scheduler.elastic() ).doOnNext( user -> BlockRepository.saveUser( user ) ).then()
````