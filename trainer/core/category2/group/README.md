* I'll show you how to use group  module of ansible
* Short documentation about command
```
Manage presence of groups on a host
```
* Example
```
ansible localhost -m group -a "name=test state=present"
localhost | SUCCESS => {
    "changed": true, 
    "failed": false, 
    "gid": 1002, 
    "name": "test", 
    "state": "present", 
    "system": false
}
```
```
ansible localhost -m group -a "name=test state=absent gid=1002 system=no"
localhost | SUCCESS => {
    "changed": true, 
    "failed": false, 
    "name": "test", 
    "state": "absent"
}
```
