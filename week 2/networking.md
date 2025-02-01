# networking

the job of os iss to abstrac(lie) about systyem(file, processors)

`find src | grep wc -l`

`ps ux` all your processies in current shell

`find . > /dev/null`

`control z`  susupend current action

`fg` means foreground, actively running and can type command

`bg` background, keep programming number

`jobs` current jobs , `Kill %1` kill the fitst job

`Kill -kill`

`pkill -9 find` use this to kill command by name

networking:

what is my ip address?

router cordinate message between machines, lan means local area network(local unit). 

to tlak to outside world, router talk to Comcast(ISP, a service company), Comcast9(SP) talk to google, google talk to youtube service

internet is a networks of networks

router send message to different networds, 

network is a graph data strcture, minimum spanning graph?

client/server model to communicate on networks.

- i have a application called client, client make request to another application called server.(laptop can have client and server at same time, os provide process illustion, 2 process 1 is client 1 is server, it could be on the same machine)
- in order for client to talk to server, you need to know the hostname(domain name, student10 cse.nd.edu)  host name translate into a ip address
- `lp -br addr` see ip address
- ip is a series of 4 numbers between 0 and 255, is just a 32 bit number
- 192.168 is a priviate local address, 127.0.0 is a machine talk back to myself
- `ifconfig` to see ip address
- you need to ip address to talk to another computer(machine) via client/server model. the way to translate name to ip address(DNS, domain name service) `host [google.com](http://google.com)` to see ip address, domain name always map ip address
- `dig` look up all dns information and meta data about domain
- in order to talk to another machine, you need to know ip and application the port as well. 80 HTTP, 22 SSH, 443 HTTPS. `ss -tlpn` to see the ports are open on the current machine
- `nmap` let you scan another machine `nmap -v -Pn`

- relation ship betwen ip address and port?

- protocal: rules to talk to each other `nc google.com 80`
- client and server are just communciataing text, which is like a unix fosswire
- `wget` is a http client, to download files
- `curl`

what is nd’s ip address

computer are magical but not magic, cs is about trade off

ssh to log into another machine

when use domain name, DNS system use names translate to IP address

you need IP address and port to talk to server

`ss -tlpn` know the flags normal

know ports on another machine : nmap -v -PN dredd.h4x8r .space

host weasel.h4x8r.space

2 domains name results in the same IP address, there can me multiple domain name results in same machine(IP Address)

web server need to know which sub domain need to go to, the domain name can have multiple IP address, IP and domain names not 1 to 1 but many to many relationships

protocal http speaks language

`curl , wget` download things

latency and bandiwth need to be think about for network perfomance, use ping to measure latency

`ping -c 1 dredd.h4x8r.space`

ping is a measure of delay

bandwidth, is capcity over time, is how much you can carry instead of delay, to measure: —kb/s

`tracerroute google.com`: track how many machines need to be routered to 

transfer files from one machine to another: `sftp` , it use ssh to transfer protocal, it gives you a limited SHell, check hash to see if the files are the same(sha1sum bashrc.txt)

`scp` and `sftp`, both transfer a file local to a student machinem transfer files betwween 2 machines