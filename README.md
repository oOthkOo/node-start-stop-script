nodejs-start-stop-script
========================

A Ubuntu start-stop-daemon script to restart NodeJS server in a easy way.

Configuration
-----

Change parameters values this script

``` sh
DAEMON_PID="{your node server pid file}"
DEAMON_LOG="{your node server log file}"
DEAMON_OPT="{your app.js file} > $DEAMON_LOG"
DAEMON_USER="{your user id}:{your group id}"
```

Install
-----

``` sh
$ sudo cp node /etc/init.d/
$ sudo chmod +x /etc/init.d/node
$ sudo update-rc.d node defaults
```
Usage
-----

``` sh
$ sudo /etc/init.d/node start
$ sudo /etc/init.d/node stop
$ sudo /etc/init.d/node restart
```

Uninstal
-----

``` sh
$ sudo update-rc.d -f node remove
```
