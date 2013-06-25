Ubuntu NodeJS daemon script
========================
A Ubuntu script to daemonize NodeJS server in a easy way.
Features
-----
 * Ubuntu compatible
 * Stop NodeJS properly
 * LOG file support
 * PID file support
 * User uid:gid support
 
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
$ sudo cp node-server node-exec /etc/init.d/
$ sudo cd /etc/init.d/
$ sudo chmod +x node-server node-exec
$ sudo update-rc.d node-server defaults
```
Usage
-----
/etc/init.d/node-server {start|stop|status|restart|force-reload}
``` sh
$ sudo /etc/init.d/node-server start
$ sudo /etc/init.d/node-server stop
$ sudo /etc/init.d/node-server restart
```
Uninstal
-----
``` sh
$ sudo cd /etc/init.d/
$ sudo update-rc.d -f node-server remove
$ sudo rm -f /etc/init.d/node-exec
```
