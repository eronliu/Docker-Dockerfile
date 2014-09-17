Docker memcached install
========
build
---------
> docker build -t <username>/memcached .

Run memcached
---------

> docker run -d -p 11211:11211 <username>/memcached

test memcached Connection
-------------
* telnet localhost 11211
* Trying 127.0.0.1...
* Connected to localhost.
* Escape character is '^]'.
* stats
* STAT pid 1
* STAT uptime 165
* ................
