Skywire Setup with ansible
===

This asumes you are using Orange Pi Prime and are using Armbian ubuntu version from https://www.armbian.com/orange-pi-prime/

 - Assign Static allocation in dhcp for the pis

```sh
apt-get -y remove ubuntu-desktop^ && apt-get -y install openssh-server
```

 - set hostname in /etc/hostname 
 - userdel initially created user

```sh
apt update && sudo apt -y upgrade
apt -y autoremove
apt -y install python
reboot
```

 - Copy hosts.file to hosts and modify each pi prime ip address
 - Now run ansible
```sh
ansible-playbook -i hosts site.yml
```
 - Go to skynode01:8080, default password is 1234