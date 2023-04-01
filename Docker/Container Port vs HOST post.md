- Multiple containers can run in your host machine
-  A machine has only certain ports available
-  For machine , only one port can be accesed at a time
- **But !!! Two containers can run on same Container port as long as they are binded to two different machine ports**
- You have to do port binding in order to reach the container , else container is unreachable
## Some info on port binding
- **Docker containers can connect to the outside world without further configuration, but the outside world cannot connect to Docker containers by default.**
- A bridge network is created (with the name `bridge`) when you install Docker. Every outgoing connection appears to originate from the host’s IP space; Docker creates a custom [iptables](iptables.md) [masquerading rule](http://www.tldp.org/HOWTO/html_single/Masquerading-Simple-HOWTO/).