nodejs-start-stop-script
========================

A Ubuntu start-stop-daemon script to restart NodeJS server in a easy way.

Configuration
-----

Change parameters values

``` txt
DAEMON_PID="{your node server pid file}"
DEAMON_LOG="{your node server log file}"
DEAMON_OPT="/{your app.js file} > $DEAMON_LOG"
DAEMON_USER="{your user id}:{your group id}"
```

Installation
-----

``` sh

```

Usage
-----

``` sh
$ /etc/init.d/node start
$ /etc/init.d/node stop
$ /etc/init.d/node restart
```
