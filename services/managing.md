# Managing Services

Older systems use **init**
Modern systems use **SystemD**

## on SystemD distros

### **systemctl**

- Manages system and service confiugrations and operations
- **systemctl status**
  - lists services and process numbers
- **systemctl status \<service>**
  - will show if service is **active** (running)
  - **Enabled** status means starts at boot time
- **systemctl disable \<service>**
  - removes from start on boot
- **systemctl stop \<service>**
  - stops service running, makes it inactive/dead
- **systemctl enable**
- **systemctl start**
- **systemctl restart**

Running/enabling a service creates a symlink to the service
