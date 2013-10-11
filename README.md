Ripple Plex
===========
Ripple Plex (aka ripple-plex) is a proxy for the ripple websocket protocol. Ripple plex
performs load balancing, caching and distribution of subscriptions among other functionality.

Installation
------------
Omnibus tested with Ubuntu [12|13]\.[04|10] with correct everything. If you like, repackage.
We're also on rubygems for the adventurous as ripple-plex.
* Execute:
```bash
$ sudo apt-add-repository ppa:jaesharp/ripple-plex
$ sudo apt-get update
$ sudo apt-get install ripple-plex
```

Basic Configuration
-------------------
* By default, we have no backends and all connection attempts to the specified client websocket will fail
* To enable rippled backends, edit the configuration file at ```/etc/ripple-plex/backends.yml``` to look like this:
```yml
backends:
  - ip: <your rippled ip address>
    public_websocket_port: :<your rippled public websocket port>
  - [another server, optional]
```
