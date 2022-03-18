---
title: "About the @lru-cache Decorator"
date: 2022-03-18T15:54:27Z
draft: false
---
Have come across a caching decorator called `@functools.lru_cache`. I looked up the [docs](https://docs.python.org/3/library/functools.html#functools.lru_cache) and they say it is used to save up to the max size of most recent calls. In the context of plugins it caches the import string the first time it is used to save having to instantiate it every time. 
