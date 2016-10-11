Ubuntu NodeJS daemon script
========================
[![SlugBay Badge](https://www.slugbay.com/pictures/badges/slugbay-simple.svg)](https://www.slugbay.com)

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
Change this parameter value in node-server script :
(ex: user:user)
``` sh
DAEMON_USER="{your-user-uid:your-user-gid}"
```
Change theses parameters value in node-exec script :
(ex: /var/lib/node)
``` sh
DAEMON_APP_DIR="{your-app-directory}"
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
