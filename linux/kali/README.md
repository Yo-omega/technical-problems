# KALI:
## Network:
- ### How to fix no ethernet adapter in Kali Linux.
    1. Go to /etc/network/
    2. Open the file `interfaces`  with a text editor (nano/vim).
    3. Add the following : 

             auto eth0
             iface eth0 inet dhcp

    4. Reboot the system
