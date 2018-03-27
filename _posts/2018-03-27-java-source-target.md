---
title: "Cross-Compilation Options: java -source -target"
comments: true
tags:
  - Crossover Compilation
  - java
---

Notes to myself to unwrap my head about this crossover compilation thingy.

<!--more-->

### Cross-Compilation Options

  Given JDK 8
  when -source 1.8 -target 1.6
  then **Cannot work**

  Given JDK 8
  when -source 1.8 -target 1.7
  then **Cannot work**

  Given JDK 8
  when -source 1.6 -target 1.6
  then **Can work**

  Given JDK 8
  when no source no target
  then it means -source 1.8 -target 1.8

And may use [Animal Sniffer Maven Plugin](http://www.mojohaus.org/animal-sniffer/animal-sniffer-maven-plugin/) to sniff 
out incompatibilites in the API