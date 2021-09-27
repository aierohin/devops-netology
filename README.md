1. 	Linux:  
	ip -br link   
	lo               UNKNOWN        00:00:00:00:00:00 <LOOPBACK,UP,LOWER_UP>   
	eth0             UP             9a:13:28:75:56:09 <BROADCAST,MULTICAST,UP,LOWER_UP>   
	  
	Windows:  
	ipconfig /all  
	  
2.	lldp, lldpd, lldpctl  
  
3. vlan,   
	nano /etc/network/interfaces  
	auto vlan100  
	iface vlan100 inet static  
	address 192.168.1.1          
	netmask 255.255.255.0          
	vlan_raw_device eth0  
	
4.	Типы LAG:  
	●статический (на Cisco mode on);  
	●динамический – LACP протокол (на Cisco mode active)  
	  
	auto bond0  
iface bond0 inet manual  
        bond-slaves eno1 eno2  
$# bond-mode 4 = 802.3ad  
        bond-mode 4  
        bond-miimon 100  
        bond-downdelay 200  
        bond-updelay 200  
        bond-lacp-rate 1  
        bond-xmit-hash-policy layer2+3  
        up ifconfig bond0 0.0.0.0 up  
  
auto bond0.123  
iface bond0.123 inet static  
        address 10.123.0.3  
        netmask 255.255.255.0  
        mtu 1500  
        gateway 10.123.0.1  
        vlan-raw-device bond0  
        post-up ifconfig bond0.123 mtu 1500  
		  
5.	8 адресов, 2 зарезервированно(адрес сети и бродкаст), 6 можно использовать для хостов.  
	32 сети /29  
	10.10.10.0/29, 10.10.10.8/29, 10.10.10.16/29  
	  
6.	1. Requested size: 50 hosts  
	Netmask:   255.255.255.192 = 26 11111111.11111111.11111111.11 000000  
	Network:   100.64.0.0/26        01100100.01000000.00000000.00 000000  
	HostMin:   100.64.0.1           01100100.01000000.00000000.00 000001  
	HostMax:   100.64.0.62          01100100.01000000.00000000.00 111110  
	Broadcast: 100.64.0.63          01100100.01000000.00000000.00 111111  
	Hosts/Net: 62                    Class A  
	  
7.	Linux:  
	arp -n  
	Address                  HWtype  HWaddress           Flags Mask            Iface  
	172.16.254.1             ether   02:63:e7:d8:d6:89   C                     eth0  
	  
	arp -d address   
	  
	Windows:  
	netsh interface ip delete arpcache  
