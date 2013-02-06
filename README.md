A handful homemade set of munin plugins
=========

The idea behind the scripts was to avoid the need of installing common needed extensions in order to communicate with the service.

Usually, in order to query [memcached](http://memcached.org/) you would install the [PECL extension](http://pecl.php.net/package/memcached) in PHP, same for [gearmand](http://gearman.org/)

These scripts make use of the low-level interface of sockets in PHP to open and query the service.

Currently implemented services
=========

 - Memcached
 - Gearmand


Usage
=====

Just drop them as you would usually do with other munin plugins and you will be running.

By default the plugins assume you want to monitor localhost (127.0.0.1) and the default port for the service.

If you need to monitor another host or a non-standard port you can do it by changing the name of the symbolic link to the plugin.

For example: (to query the host 192.168.0.132 port 11212) you should name the symbolic link:

`memcache_connections-192.168.0.132-11212`

The script will parse the name and connect to the given host/port


Suggestions? 
=======

Sure. Just drop me a line or open an issue.


License
=======

Copyright (c) 2013 Gabriel Sosa

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE. 

