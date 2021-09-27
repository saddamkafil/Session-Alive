### How to configure git-bash from disconnecting 

####Step-1 : On server side edit below line 
```
/etc/ssh/sshd_config 
```
ClientAliveInterval 60
ClientAliveCountMax 3

####setp2: Restart sshd
```
systemctl restart sshd
```
or 
```
sudo /etc/init.d/sshd restart
```

####Step3: In git bash add below lines in 
``` 
~/.ssh/config
```
### Lines to be added are 
```
Host *
    ServerAliveInterval 20
    TCPKeepAlive no
```
Restart gitbash or exit and reopen gitbash 

#Done
