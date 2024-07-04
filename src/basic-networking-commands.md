# Basic Networking Commands (ping, ifconfig, ip)

In this section, we'll cover essential networking commands in Linux for network troubleshooting and configuration.

## `ping`

The `ping` command is used to test the connectivity between two networked devices by sending ICMP echo request packets and waiting for ICMP echo reply packets.

### Syntax:
```bash
ping [options] host_or_ip_address
```

### Examples:
```bash
ping www.example.com   # Ping a domain name
ping 192.168.1.1   # Ping an IP address
ping -c 4 192.168.1.1   # Send 4 ICMP echo request packets
```

### Common Options:
- -c count: Number of ICMP echo requests to send.
- -i interval: Specify the interval between packets.
- -s packetsize: Set the size of the ICMP packets.
  
## `ifconfig` (Interface Configuration)
The `ifconfig` command is used to configure and display network interface parameters.

Syntax:
```bash
ifconfig [interface] [options]
```

### Examples:
```bash
ifconfig eth0   # Display configuration of interface eth0
ifconfig eth0 up   # Activate (up) interface eth0
ifconfig eth0 down   # Deactivate (down) interface eth0
```
Note: ifconfig is being replaced by ip command in modern Linux distributions.

## `ip` (IP Route)
The `ip` command is a versatile tool for configuring network interfaces, routing tables, and managing network devices and their addresses.

Syntax:
```bash
ip [options] object command
```

### Examples:
```bash
ip addr show   # Show IP addresses assigned to all network interfaces
ip link set dev eth0 up   # Activate (up) interface eth0
ip route show   # Display the routing table
```
Note: ip command provides more features and flexibility compared to ifconfig.

# Summary
These basic networking commands (ping, ifconfig, ip) are essential for network diagnostics, interface configuration, and routing management in Linux. Understanding how to use these commands is valuable for both network administrators and Linux users.

For more information and detailed options, refer to the respective manual pages using the man command (e.g., man ping, man ifconfig, man ip).
