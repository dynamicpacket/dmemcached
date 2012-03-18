Dmemcached
==========

This software creates an HA memcached cluster with configurable replicas to avoid key 
loss on a specific node failure. Each node is treated as a hash bucket and, when configured
with enough replicas, can tolerate multiple node failures without loosing any keys. Keys are
distributed along buckets using consistent hashing, so it is safe to run multiple instances
of this software inside your network, provided the config file is the same on each dmemcached
instance.

Caveats
-------

Memcached's biggest enemy is network latency. If you wish to utilize this software for multi-site
replication, be aware that the performance can only be as good as latency between both locations.
That being said, if some memcached buckets are local vs remote, latency could be much lower or 
higher when retrieving certain keys depending on which bucket it gets stored in.

Contributing
------------

Want to contribute? Great! Fork this repository or send patches to support  a t  dynamicpacket  d o t  com 
or fork this repository and request a merge with your changes.

