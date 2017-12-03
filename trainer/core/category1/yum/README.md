* I'll show you how to use yum module of ansible
* Short documentation about command
```
Installs, upgrade, downgrades, removes, and lists packages and groups with the yum package manager.
```
* Example
```
/opt/ansible/ansible# ansible localhost -m yum -a update_cache=yes
localhost | SUCCESS => {
    "cache_update_time": 1510591591, 
    "cache_updated": true, 
    "changed": true
}
```
```
ansible localhost -m yum -a "name=httpd state=present"
```
