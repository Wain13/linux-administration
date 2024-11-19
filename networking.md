# Networking

# IP Address

    - ifconfig
      - works for most linux and unix-like systems
    - ip addr
      - used on newer linux systems
    - usually set in files like **/etc/sysconfig/network-scripts/ifcfg-eth0**
      - newer systems (Fedora) often use NetworkManager:
      - **/etc/NetworkManager/**

# MAC Address

    - ip addr
    - ifconfig

# Hostname

    - **hostname**
      - keyword will display host name
    - set in **/etc/resolv.conf**

# DNS

    - /etc/resolv.conf
    - sets nameserver
  
# Testing utilities

    - ping
    - traceroute