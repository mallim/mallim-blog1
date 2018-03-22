---
title: "Mybatis Batch mode"
comments: true
tags:
  - mybatis
  - java
---

IBATIS/Mybatis has the same underlying thing to watch out:

````
To get benefit from batch executor, all the statements must be the same (it internally uses java.sql.PreparedStatement#addBatch()).
If you use <foreach />, the statement changes and MyBatis has to create a new statement, so performance will get worse.
````

<!--more-->

[Bulk insert (multi-row vs. batch) using JDBC and MyBatis](http://blog.harawata.net/2016/04/bulk-insert-multi-row-vs-batch-using.html?m=1)
there is performance indicator in here

**Option B:** you might just have to look at how to manipulate the sql as shown in https://stackoverflow.com/questions/19559418/oracle-insert-all-vs-insert

