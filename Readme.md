# remote acess ssh


##### Steps 1 - Config ssh in your Machine remote.

``` sh 
sudo apt install ssh
cd /etc/ssh

```

##### Step 2 -  Open PORT in the file sshd_config.

``` sh
sudo nano sshd_config
Port 22 to exemple 2225

```
##### Step 3 -  Add Port and Ip Machine in your router.
``` sh 
The port is same like sshd_config exemple: 2225
Add IP machine remote in your router exemple: 192.168.1.xxx
  
```
##### Step 4 - Give access port in you machine remote.
``` sh 
Exemple Port: 2225
Command linux: sudo iptables -A INPUT -p tcp --dport 2222 -j ACCEP

```
##### Step 5 - Restart ssh 
``` sh 
sudo /etc/init.d/ssh restart
```

##### Step 6 - Connect with your client other computer
```
sudo ssh usernamecomputerRemote@192.168.1.xxx -p 2225
Enter password machine remote

 
 ```