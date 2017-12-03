* I'll show you how to use template  module of ansible
* Short documentation about command
```
Template takes a file (template) from host,changes variables based on Jinja2 filtering,and copies it to the remote destination.
```
* Example
```
ansible  localhost -m template -a "src=test.j2 dest=/home/testing"
localhost | SUCCESS => {
    "changed": true, 
    "checksum": "9bc0cb2ed6def7afea9395ab78790a0c79c64ab1", 
    "dest": "/home/testing", 
    "failed": false, 
    "gid": 0, 
    "group": "root", 
    "md5sum": "18697449d7c48cf32cdd4f14857e68ee", 
    "mode": "0644", 
    "owner": "root", 
    "size": 5, 
    "src": "/root/.ansible/tmp/ansible-tmp-1510643032.01-155745522829853/source", 
    "state": "file", 
    "uid": 0
}
```
```
ansible  localhost -m template -a "src=test.j2 dest=/home/testing owner=root group=root mode=0755 backup=yes"
localhost | SUCCESS => {
    "changed": true, 
    "checksum": "9bc0cb2ed6def7afea9395ab78790a0c79c64ab1", 
    "dest": "/home/testing", 
    "failed": false, 
    "gid": 0, 
    "group": "root", 
    "md5sum": "18697449d7c48cf32cdd4f14857e68ee", 
    "mode": "0755", 
    "owner": "root", 
    "size": 5, 
    "src": "/root/.ansible/tmp/ansible-tmp-1510643143.94-187312371172942/source", 
    "state": "file", 
    "uid": 0
}
```

