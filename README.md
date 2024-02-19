root@b058a76ec893:/etc/freeradius/sites-enabled# systemctl status freeradius
freeradius.service - FreeRADIUS multi-protocol policy server
    Loaded: loaded (/usr/lib/systemd/system/freeradius.service, enabled)
    Active: inactive (dead)
root@b058a76ec893:/etc/freeradius/sites-enabled# netstat -tuln | grep 1812
udp        0      0 127.0.0.1:18120         0.0.0.0:*                          
udp        0      0 0.0.0.0:1812            0.0.0.0:*                          
udp6       0      0 :::1812                 :::*                               
root@b058a76ec893:/etc/freeradius/sites-enabled# 
