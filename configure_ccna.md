DHCP configuration
==================

## 1. Enabling the Cisco IOS DHCP Server and Relay Agent Feature

* Comand:
```
Router(config)# service dhcp
```

* Purpose:
  * Enalbles the Cisco IOS DHCP server and relay features on your router.
  * Use `no` from of this command to disable the Cisco IOS DHCP server and relay agent

## 2. Configuring a DHCP Database Agent of Disabling DHCP Conflict Logging
```
A DHCP database agent is any host - for example, an FTP, TFTP, or rcp() server - that stores the DHCP bindings database.
```

* Command:
```
Router(config)# ip dhcp database url [timeout seconds  write-delay seconds]
```

* Purpose:
  * Configures the database agent and the interval between database updates and database transfers.

* Command:
```
Router(config)# no ip dhcp conflict logging
```

* Purpose:
  * Disables DHCP address conflict logging.

## 3. Exluding IP Adresses

* Command:
```
Router(config)# ip dhcp excluded-address low-address [high-address]

* Purpose:
  * Specifies the IP addresses that the DHCP Server should not assign to DHCP clients.

## 4. Configuring a DHCP Address Pool

### 4.1 Configuring the DHCP Address Pool Name and Entering DHCP Pool Configuring Mode

* Command:
```
Router(config)# ip dhcp pool name
```

* Purpose:
  * Creates a name for the DHCP Server address pool and places in DHCP pool configuration mode (identified by the dhcp-config# prompt).

### 4.2 Configuring the DHCP Address Pool Subnet and Mask

* Command:
```
Router(dhcp-config)# network network-number [mask | /prefix-length]
```

* Purpose: 
  * Specifies the subnet network number and mask of DHCP address pool.
  * The prefix length specifies the number of bis that comprise the address prefix. The prefix is an alternative way of specifying the network mask of the client. The prefix length must be preceded by a forward slash (/).

### 4.3 Configuring the Domain Name for the Client

* Command;
```
Router(dhcp-config)# domain-name domain
```

* Purpose:
  * Specifies the domain name for the client.

### 4.4 Configuring the IP Domain Name System Servers for the Client

* Command:
```
Router(dhcp-config)# dns-server address [address2 ... address8]
```

* Purpose:
  * Specifies the IP address of a DNS server that is available to a DHCP client. One IP address is required; however, you can specify up to eight IP addresses in one command line.

### 4.5 Configuring the NetBIOS Windows Internet Naming Service Servers for the Client

* Command:
```
Router(dhcp-config)# netbios-name-server address [address2 ... address8]
```

* Purpose:
  * Specifies the NetBIOS WINS server that is available to a Microsoft DHCP client. One address is required; however, you can specify up to eight addresses in one command line.

### 4.6 Configuring the NetBIOS Node Type for the Client

* The NetBIOS node type for Microsoft DHCP clients can be one of four settings:
  * broadcast
  * peer-to-peer
  * mixed
  * hybrid

* Command:
```
Router(dhcp-config)# netbios-node-type type
```

* Purpose:
  * Specifies the NetBIOS node type for a Microsoft DHCP client.

### 4.7 Configuring the Default Router for the Client

The IP address of the default router should be on the same subnet as the client.

* Command
```
Router(dhcp-config)# default-router address [address2...address8]
```

* Purpose:
  * Specifies the IP address of the default router for a DHCP client. One IP address is required; however, you can specify up eight addresses in one command line.

### 4.8 Configuring the Address Lease Time

By default, each IP address assigned by a DHCP Server comes with a one-day lease, which is the amount of time that the address is valid. To change the lease value for an IP address, use the following command in DHCP pool configuration mode:

* Command:
```
Router(dhcp-config)# lease {days [hours][minutes] infinite}
```

* Purpose:
  * Specifies the duration of the lease. The default is a one-day lease.
  * Use the `show ip dhcp binding` to display the lease expiration time and date of the IP address of the host.









































