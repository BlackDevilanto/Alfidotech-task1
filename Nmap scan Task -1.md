# Alfidotech-task1
Nmap Scanning Report
-----------------------
Scan Target IP: 192.168.75.128
Scan Type: Default TCP SYN scan
Nmap Version: 7.94SVN
Host Status: Host is up (Latency: 0.0015s)

Open TCP Ports & Services
---------------------------
Port	    State Service
21/tcp	  open	ftp
22/tcp	  open	ssh
23/tcp	  open	telnet
25/tcp	  open	smtp
53/tcp	  open	domain
80/tcp	  open	http
111/tcp	  open	rpcbind
139/tcp	  open	netbios-ssn
445/tcp 	open	microsoft-ds
512/tcp	  open	exec
513/tcp	  open	login
514/tcp	  open	shell
1099/tcp	open	rmiregistry
1524/tcp	open	ingreslock
2049/tcp	open	nfs
2121/tcp	open	ccproxy-ftp
3306/tcp	open	mysql
5432/tcp	open	postgresql
5900/tcp	open	vnc
6000/tcp	open	X11
6667/tcp	open	irc
8009/tcp	open	ajp13
8180/tcp	open	unknown


Observations & Notes
--------------------------
- Multiple remote access services are open (SSH, Telnet, VNC).
- Several legacy/possibly insecure services found (e.g., Telnet, exec, login, shell).
- Database ports open (MySQL, PostgreSQL) – might be targets for SQL injection or password attacks.
- Port 8180 is running an unknown service, which should be further analyzed (e.g., using 'nmap -sV -p 8180').
Recommendations
--------------------------------
- Disable unused or insecure services like Telnet, exec, and shell.
- Ensure strong authentication and firewall rules for open services.
- Monitor traffic on uncommon open ports (1524, 8009, 8180).
- Perform a version scan using 'nmap -sV 192.168.75.128' to identify service versions.
