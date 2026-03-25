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
Donations
-----

:heart: Donations are always welcome :heart:.

### Buymeacoffee

[<img height="55px" src="https://raw.githubusercontent.com/oOthkOo/oOthkOo/main/assets/bmac-btn.svg">](https://buymeacoffee.com/oothkoo)

### Crypto

Coins | Symbols | Addresses
--- | --- | ---
<img width="32" src="https://raw.githubusercontent.com/oOthkOo/oOthkOo/main/assets/btc.svg" alt="Bitcoin"/> | BTC | 3B52fbzNFQTaKZxWf5GrCUsASD2UP8na4A
<img width="32" src="https://raw.githubusercontent.com/oOthkOo/oOthkOo/main/assets/eth.svg" alt="Ethereum"/> | ETH | 0x1C389f1f85Cdb3C2996b83fAc87E496A80698B7C
<img width="32" src="https://raw.githubusercontent.com/oOthkOo/oOthkOo/main/assets/sol.svg" alt="Solana"/> | SOL | F14pWhGjGLcCF8RMk4JhbK2kD49iBBwa9KFygRJo54Fm
