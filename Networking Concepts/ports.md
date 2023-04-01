- Virtual point where network connection starts and ends
- Managed by the OS
- Associated with a specific process or service
- Ports allow computers to differentiate between different kinds of service
- Network layer entity, like TCP and UDP


## Check open ports in linux
1.  Viewing open files
`sudo lsof -i -P -n | grep LISTEN`

2.  Viewing the Internet network services list
	`less /etc/services`
3. Using ss
	`sudo ss -tulwn | grep LISTEN`
	![Pasted image 20230113105324](Pasted%20image%2020230113105324.png)