# SolvedProblems
give the solutions of solved problems that I interface randomly. 


#### How to fix no ethernet adapter in Kali Linux.
1. go to /etc/network/
2. open the file " interfaces "  with text editor.
3. type the following :
   
       auto eth0
       iface eth0 inet dhcp

5. reboot the system
