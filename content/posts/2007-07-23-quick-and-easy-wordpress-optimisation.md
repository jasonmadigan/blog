---
title: Quick & Easy Wordpress Optimisation
date: 2007-07-23T21:00:00
---

Here's two quick and easy steps you can take to increase your Wordpress
sites speed:

Enable Wordpress's Object Caching
---------------------------------

Add define('ENABLE\_CACHE', true); to your wp-config.php to enable
Wordpress's built in [object
caching](http://codex.wordpress.org/Function_Reference/WP_Cache) and
Wordpress will begin caching all sorts of database queries resulting in
an instantaneous performance boost.

Install WP-Cache 2
------------------

[WP-Cache](http://mnm.uib.es/gallir/wp-cache-2/) is a plugin which
serializes and caches posts to disk for quick retrieval. It's also smart
enough to keep serialized data on the disk up to date so it won't serve
stale content.
