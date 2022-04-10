# mstsc.js

![Mstsc.js Logo](./client/img/mstsc.js.png)

**Mstsc.js** ist ein reiner Javascript-Client für Microsoft RDP (Remote Desktop Client), der nodejs, [**node-rdpjs**](https://github.com/citronneur/node-rdpjs) und socket.io verwendet . Es ermöglicht Ihnen, über einen Webbrowser (optimiert für Firefox, aber auch kompatibel mit Chrome und Internet Explorer 11) eine Verbindung zu jeder Terminalserver-kompatiblen Anwendung herzustellen.

<img src='./img/mstsc.js.login.png' width=200/>
<img src='./img/mstsc.js.connect.png' width=200/>
<img src='./img/mstsc.js.explorer.png' width=200/>

## Installieren

Letzte Version installieren:

```
npm installiert mstsc.js
```

Letzten Dev-Commit installieren:

```
Git-Klon https://github.com/citronneur/mstsc.js
cd mstsc.js
npm installieren
Knotenserver.js
```

## Wie funktioniert es ?

### Front-end

Das Front-End ist für die Bitmap-Dekomprimierung. Die dafür zuständige Datei ist "rle.js" und zusammen mit [**Emscripten**] einer Compiler-Toolchain
(https://github.com/kripken/emscripten) aus [rle.c](https://raw.githubusercontent.com/citronneur/mstsc.js/master/ obj/rle.c), stammt dies aus der rdesktop-Quelle.
Für die Bindung mit dem Backend verwendet die Anwendung *socket.io* und *canvas*. mstsc.js- 

### Back-end

Die Backend-Anwendung verwendet nodejs, express und socket.io als Webserver. Das Hauptziel des Backends ist es, ein Proxy zwischen dem Webbrowser und dem Terminalserver zu sein. Es verwendet [**node-rdpjs**](https://github.com/citronneur/node-rdpjs) für seinen RDP-Client.
## Cozy-Cloud

Mstsc.js is designed to work with **Cozy-Cloud**!

![Cozy Logo](https://raw.github.com/mycozycloud/cozy-setup/gh-pages/assets/images/happycloud.png)

[**Cozy**](http://cozy.io) is a platform that brings all your web services into the
same private space.  With it, your web apps and your devices can share data
easily, providing you
with a new experience. You can install Cozy on your own hardware where no one
is spying.
