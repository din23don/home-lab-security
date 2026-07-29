# Network traffic analysis with wireshark 

## Tool

Wireshark was used to analyze network traffic between Kali Linux and Ubuntu Server.

## Lab Network

Network type:

Host-Only Network

Ubuntu Server IP:

```text
192.168.56.101
```

Kali Linux connects to Ubuntu through this network.

## Capture process

Steps:

1. Open Wireshark
2. Select the Host-Only network interface
3. Start packet capture
4. Generate network traffic using ping and SSH

Commands used:

```bash
ping 192.168.56.101
```

## Display filters

ICMP:

```text
icmp
```

SSH:

```text
tcp.port
```

## Resault 

Wireshark successfully captured ICMP and SSH between Kali Linux and Ubuntu Server.


