# Static_IP

Configuring Static IP address on Ubuntu Server #

ip link

sudo nano /etc/cloud/cloud.cfg.d/99-disable-network-config.cfg


sudo nano /etc/netplan/01-netcfg.yaml

network:
  version: 2
  renderer: networkd
  ethernets:
    ens3:
      dhcp4: no
      addresses:
        - 192.168.121.221/24
      gateway4: 192.168.121.1
      nameservers:
          addresses: [8.8.8.8, 1.1.1.1]
          
          
          
sudo netplan apply

ip addr
