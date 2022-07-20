# golibs

This repository contains several useful functions and interfaces for Go:

* Cache - in-memory cache with LRU, limits and statistics
* Log - logger with configurable log-level on top of standard "log"
* File:
    * safe file writing
* JSON:
    * JSON format helper functions
* Utils:
    * hostname validator


## Cache

A quick example:

    conf := cache.Config{}
	conf.EnableLRU = true
	c := cache.New(conf)
    c.Set([]byte("key"), []byte("value"))
    val := c.Get([]byte("key"))
