* I'll show you how to use service module of ansible
* Short documentation about command
```
Controls services on remote hosts.
```
* Example
```
ansible localhost -m service -a "name=nginx state=restarted"
localhost | SUCCESS => {
    "changed": true, 
    "failed": false, 
    "name": "nginx", 
    "state": "started"
}
```
```
ansible localhost -m service -a "name=nginx state=stopped"
localhost | SUCCESS => {
    "changed": true, 
    "failed": false, 
    "name": "nginx", 
    "state": "stopped"
}
```
```
ansible localhost -m service -a "name=nginx state=restarted enabled=yes"
localhost | SUCCESS => {
    "changed": true, 
    "enabled": true, 
    "failed": false, 
    "name": "nginx", 
    "state": "started"
}
```
