RDP Web
======
This project will be a gateway for seamless access to your RDP-Sessions in any HTML5-compliant browser. 
In particular it relies on the features
* Canvas (http://www.w3.org/TR/2dcontext/) 
* WebSockets (http://www.w3.org/TR/websockets/) 

The server side WebSockets implementation handles current RFC6455
(http://tools.ietf.org/html/rfc6455) only, so browsers that implement
the older drafts do *not* work. With RFC6455 being raised to the
"Proposed Standard" level, this should change now really soon.

On the server side, a standalone daemon - written in C++ - provides a
Web page via HTTPS (or HTTP, if configured) and uses FreeRDP libs to
connect as a client to any RDP session.

### Installation ###
**Automated build/install script**::
```sh
setup-all.sh
```
**Unattended install script**
```sh
./setup-all.sh -f -i -d
```
* Force to run as root user (-f)
* Install all dependency packages (-i)
* Remove conflicting packages (-d)
