---
title: '6 Database Optimization Techniques'
date: 2024-01-16T09:45:22+07:00
lastMod: 2024-01-16T09:45:22+07:00
tocopen: false
description: "<enter description here>"
summary: "<Enter summary here>"
tags: ["Database", "Optimize"]
---

## 1. Indexing

> _**Index** is a data structure which is used to locate and fast access data in tables or views_

* Indexing helps reducing the amount of access to memory during query execution by establishing organized structures, adding db engine in promptly identifying rows that meet specified conditions in `where` clause.

</br>

* Although indexing boosts the perfomance of queries, it will be a trade off for the write operations. So it
