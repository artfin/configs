My configs for ```vim``` and ```i3wm```:
* vim: 
	* Using Vundle plugin manager 
* i3wm (config file is ~/.config/i3/config):
	*  System San Fransisco Font files should be put in ~/.fonts (just drop there all the ```.ttf```-files)

# Clean installation and preparation of Python2.7 on Ubuntu server

* preparing system configuration <br />
```sudo apt-get update``` (keeps your source list up-to-date) <br />
```sudo atp-get upgrade``` (upgrades all installed packages) <br /> 
```sudo apt-get dist-upgrade```(upgrade with some smart conflist-resolution system)

* installing python: <br />
``` sudo apt-get install python2.7```

* installing and upgrading ```pip```: <br />
``` sudo apt-get install python-pip python-dev build-essential``` <br />
```sudo -H python -m pip install --upgrade```

* installing ```cryptography``` package: <br />
``` sudo apt-get install libssl-dev libffi-dev python-dev```<br />
``` sudo -H python -m pip install cryptography```

* list of packages: <br />
 1. Beautiful soup: ```sudo -H python -m pip install bs4```
 2. dateutil.parser: ```sudo apt-get install python-dateutil```
 3. Crypto: ```sudo -H python -m pip install pycrypto```
 4. builtins: ```sudo -H python -m pip install future```
 5. lxml: ```sudo -H python -m pip install lxml``` (HTML-markup parser for ```bs4```)

# Crontab info

* Setting environment variables  <br />
```SHELL=/bin/sh```  <br />
```PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin```

* ```timeout``` for terminating hanging processes  <br />
``` /usr/bin/timeout 5m```

# Example 
// Environment variable <br />
```SHELL=/bin/sh```
```PATH=/usr/local/sbin:/usr/local/bin:/bin:/usr/sbin:/usr/bin```

// ----------------------------------------------------- <br />
// ```ps axo pid,etime,args -- to see id of process and  its execution time``` <br />
// ----------------------------------------------------- <br />

// ----------------------------------------------------- <br />
// adding timeout command to terminate hanging processes <br />
// ----------------------------------------------------- <br />

```*/2 * * * * /usr/bin/timeout 3m /home/ubuntu/Steamdaemon/steamdaemon/usr/terol983/scripts/_buyorder_checker.sh``` <br />
```*/2 * * * * /usr/bin/timeout 3m /home/ubuntu/Steamdaemon/steamdaemon/usr/terol983/scripts/_sellorder_checker.sh``` <br />
```0,20,40 * * * * /usr/bin/timeout 9m /home/ubuntu/Steamdaemon/steamdaemon/usr/terol983/scripts/_buyorder_installer.sh```

