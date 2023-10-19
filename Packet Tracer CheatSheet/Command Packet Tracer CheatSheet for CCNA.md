
### <h3 align = "center"> **Level modes** :</h3> 
#### **User exec mode** :
 Most restricted access level. Limited commands that allow the user to **view statistics and perform basic troubleshooting**.

---
#### **Privileged exec mode**:

Tipically requires a password for access. The mode is usually used for some of the following purposes : **view, save, debug, erase device configurations**.

---
#### **Global configuration mode** :
Commands used to configure the device. This mode is used to **update, change or delete** existing settings. 

---
#### **Interface configuration mode** :
Configure a **physical interface of the device**.

---
## <h3 align = "center">**Command list :** </h3>

| Navigation Commands ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ |                                    Action |
| -------------------------   |  ------------------- |
| ``?`` | Display a list of available commands. |
| ``Device> enable`` | Enables privileged exec mode. |
| ``Device# disable`` | Exit the privileged exec mode |
| ``Device# configure terminal``  | Enters the global configuration mode |
| ``Device(config)# interface <type> <number>`` | Access and configure a specific network interface on the device <br> <br> Example: interface GigabitEthernet0/1 |
| ``exit`` | Exits the current mode level |
| ``end`` | Get back to Privileged exec mode |
| ``do`` | Execute command from the privileged exec mode |
| ``no <command>`` | Negate or remove a configuration command or statement <br><br> Example: the command "no shutdown" means to actually enable the interface |

| Privilaged Exec Mode Commands ‎             | Action |
| ----- | ----|
| ``ping <IP>`` | Test reachability or conectivity between hosts |
| ``hostname <name>`` | Change the hostname of a device |
| ``reload`` | Reboot or restar a device |
| ``copy running-config startup-config`` | Save the current running configuration of the device to the startup configuration |
| ``show ip interface brief`` | Show available interfaces and their parameters briefly |
| ``show ip route`` | Show the routing table |
| ``show mac address table`` | Show the MAC table |
| ``show running config`` | Show the device entire active configuration |
| ``show interface <type> <number>`` | Show information about the status and configuration of a specific interface |
| ``show arp`` | Display the ARP table entries |
| ``clear arp-cache`` | Clear the ARP cache or table, removing all ARP entries |

### IPV6

Unicast
	-  Link Local Address : From FC00::/7. They are asigned from the range FE80::/10- FEB0::/10
	-  Global Unique address : From 2000::/3

Multicast:
	Well known:
	- all routes ff02::2
	- all nodes ff02::1
	Solicited node: ff02::1:ff00:0 /104 (Se usa para el arp ?)

en mi caso :
FF02::1

FF02::2

FF02::1:FF00:1

FF02::1:FF01:1



| IPv6 Commands ‎ | Action |
| ---- | ---- |
| ``ipv6 unicast-routing``|Enables IPv6 unicast routing<br><br>NOTE: remember is not enable by default|
|``ipv6 address <IPv6 address> [eui-64 option] [link-local option]`` |Configure an IPv6 address on a network interface  |
|  |  |
|  |  |
|  | |
|  |  |
| |  |

| VLAN Commands | Action |
| ---- | ---- |
|SW1(config)  |  |
| show interface trunk | |
|  |  |
|  |  |
| |  |
|  | |
|  |  |
|  |  |
| |  |

| DHCP Commands | Action |
| ---- | ---- |
| `` R1(config)# ip dhcp excluded-address <inicial>(<final>)``| Exclude some ip address |
| ``R1(config)# ip dhcp pool <Name>`` | |
| ``R1(dhcp-config)# network <network> <nask> ``|  |
| ``R1(dhcp-config)# default-router <gateway> `` |  |
| ``R1(dhcp-config)# domain-name <DNS> ``|  |
| ``R1(dhcp-config)lease <tiempo>``| |
| ``show ip dhcp binding ``| lista de direcciones dadas |
| ``show ip dhcp server statistic`` |devuelve informacion relacionada del numero de mensajes dhcp han sido enviados y recibidos |
| ``R1(dhcp-config)lease <tiempo>``| no solo es la unica configuration que vva a relay el rotuer|
| ``show running config ``| section dhcp``|despliega configuracion dhcp del router |
| ``R1(config)#no service dhcp ``| disable|
| ``R1(interface) ip helper- address <dhcp server address you want>``| |
| ``ip address dhcp ``|habilita que un equipo coja en esa interfaz la direccion ip en modo dhcp |
| ``ipv6 nd other-config-flag``| |
| ``ipv6 nd managed-config-flag`` ``| |
| ``R1(config)# ip dhcp pool <Name><dns-server x.x.x.x ``| |
| ``ipv6 dhcp server <pool name> ``|hay que decirle que pool debe usar ! |
| ``ipv6 nd managed-config-flag no-autoconfig`` ``| |
| ``ipv6 enbable ``| |
| ``ipv6 address dhcp ``| |





| DNS Commands | Action |
| ---- | ---- |
| ``ip domain-lookup`` |Enables DNS-based address translation  |
| ``ip dns server`` | Configure the device as a DNS server |
| ``ip host <name> [port] <address>``| Defines  a static hostname-to-IP address mapping on the device |
| ``ip name-server <server address>`` |Specifies to the device which hosts function as DNS (Domain Name System) servers and provide name-to-IP translation. |
| ``ip domain name <domain name>`` |Sets the default domain name (sufix) for the device. It is appended to unqualified hostnames when resolving domain names to fully qualified domain names (FQDNs)|
| ``ip address <IPv4 address> [secondary option]`` | Configure an IPv6 address on a network interface. Secondary option to add more than one address |
|  |  |

| STP Commands | Action |
| ---- | ---- |
| ``Sw2# show spanning-tree <vlan number>`` |  |
|  | |
|  |  |
|  |  |
|``SW(config-if)# spanning-tree portfast``| Only to the access ports! activate portfast mode  |
| ``SW(config-if)# spanning-tree bpduguard enable`` | |
| ``SW(config)# errdisable recovery cause bodyguard`` | Recuperarse de error bodyguard |
|  |  |
| |  |

|Static IP Routing Commands | Action |
| ---- | ---- |
| ```` |  |
|  | |
|  |  |
|  |  |
| |  |


|EtherChannel Commands | Action |
| ---- | ---- |
| ``SW1(config-if-range)# channel-group 1 mode <mode>`` | Creates |
|``SW1(config-if)# interface port-channel 1``  | |
| ``SW1(config-if)# switchport mode trunk`` | Security measures |
|``switchport trunk allowed <vlans>``  |  Security measures |
|``switchport trunk allowed <vlans>``  |  |
|``S1# show etherchannel summary`` | View the EtherChannel summary information |
| |  |
| |  |
| |  |
| |  


|FHRP Commands | Action |
| ---- | ---- |
| ``R1(config-if)#standby 1 priority 150``| For the active this commands below |
|``#standby ip 192.168.1.3`` |  |
| ``R2#stanby 1 ip 192.168.1.3`` | Comando Para los standby |  

| Security Commands | Action |
| ---- | ---- |
| ``switchport port-security`` |It can't be used in a dynamic port|
| ``switchport port-security mac-address <mac>`` | Manually configure|
| ``switchport port-security mac-address sticky``  |  |
| ``S1# show port security`` |  |
|``switchport port-security maximum 4`` |  |
|  | |
|  |  |
|  |  |
| |  |