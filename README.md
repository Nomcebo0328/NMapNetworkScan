# NMapNetworkScan
Perform a network scan to identify active hosts, open ports, and running services on the local network.
# Nmap Network Scan Results

## Objective

Perform a network scan to identify active hosts, open ports, and running services on the local network.

## Scan Command

```bash
nmap -sV 192.168.0.0/24
```

## Results Summary

### Host: 192.168.0.1

* Port 53/tcp open (DNS)
* Port 80/tcp open (HTTP)
* Port 37215/tcp filtered (Unknown)

### Host: 192.168.0.120

* Port 22/tcp open (SSH)
* Port 10250/tcp open (Unknown/Kubernetes-related service)

## Analysis

* DNS (53) indicates the device may provide name resolution services.
* HTTP (80) suggests a web management interface or web server.
* SSH (22) allows secure remote administration.
* Port 10250 is commonly associated with Kubernetes Kubelet services.
* The filtered port did not respond sufficiently for service identification.

## Conclusion

The scan identified two active hosts with several open ports providing network and management services. Further service enumeration could be performed using Nmap version detection and scripting options.
