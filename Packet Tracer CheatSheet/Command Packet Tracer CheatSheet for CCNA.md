 
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
| ``Device(config)# interface [type] [number]`` | Access and configure a specific network interface on the device <br> <br> Example: interface GigabitEthernet0/1 |
| ``exit`` | Exits the current mode level |
| ``end`` | Get back to Privileged exec mode |
| ``do`` | Execute command from the privileged exec mode |
| ``no [command]`` | Negate or remove a configuration command or statement <br><br> Example: the command "no shutdown" means to actually enable the interface |

| Privilaged Exec Mode Commands ‎             | Action |
| ----- | ----|
| ``ping [IP]`` | Test reachability or conectivity between hosts |
| ``hostname [name]`` | Change the hostname of a device |
| ``reload`` | Reboot or restar a device |
| ``copy running-config startup-config`` | Save the current running configuration of the device to the startup configuration |
| ``show ip interface brief`` | Show available interfaces and their parameters briefly |
| ``show ip route`` | Show the routing table |
| ``show mac address table`` | Show the MAC table |
| ``show running config`` | Show the device entire active configuration |
| ``show interface [type] [number]`` | Show informatio about the status and configuration of a specific interface |

| Global Configuration Mode Commands ‎ | Action |
| ---- | ---- |
|  |  |
|  | |
|  |  |
|  |  |
|  | |
|  |  |
| |  |

| Interface Configuration Mode Commands | Action |
| ---- | ---- |
|  |  |
|  | |
|  |  |
|  |  |
| |  |


| DNS Commands | Action |
| ---- | ---- |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
