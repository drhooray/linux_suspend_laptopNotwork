# linux_suspend_laptopNotwork

#test for hibernate
sudo pm-hibernate

#if work edit the config file:
sudo -i
cd /var/lib/polkit-1/localauthority/50-local.d/
gedit com.ubuntu.enable-hibernate.pkla

/*edit it*/
    [Re-enable hibernate by default in upower]
    Identity=unix-user:*
    Action=org.freedesktop.upower.hibernate
    ResultActive=yes

    [Re-enable hibernate by default in logind]
    Identity=unix-user:*
    Action=org.freedesktop.login1.hibernate
    ResultActive=yes
/*edit end*/

#Restart your laptop 
    
