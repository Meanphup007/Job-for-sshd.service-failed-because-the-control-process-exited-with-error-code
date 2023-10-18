```
sudo vim /etc/ssh/sshd_config
    Port 888
    PermitRootLogin yes 
```
```
sudo semanage port -a -t ssh_port_t -p tcp 888
```
```
sudo firewall-cmd --permanent --remove-service=ssh
```
```
sudo firewall-cmd --permanent --add-port=888/tcp
```
```
sudo systemctl start sshd
```
```
sudo systemctl enable sshd
```
```
sudo systemctl restart sshd
```
```
sudo firewall-cmd --reload
```
---
### Check port openssh: 
     sudo netstat -putan | grep ssh
### You can also use other port like port number 3 ( if it empty port )
```
sudo netstat -putan | grep :3 
```
> If it does not display any statement, it means it is empty port

> For me port 888 is empty port
### You need to have installed openssh on CMD : [Link Here](https://www.youtube.com/watch?v=Vh6z7sPI3Qk)
