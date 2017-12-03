* I'll show you how to use copy module of ansible
* Short documentation about command
```
The copy module copies a file from the local or remote machine to a location on the remote machine. Use the fetch module to copy files from remote locations to the local box. 
```
* Example
```
/opt/ansible/ansible# ansible localhost -m copy -a "src=/etc/ansible/hosts dest=/tmp/hosts"
localhost | SUCCESS => {
    "changed": false, 
    "checksum": "3fef16749c9b9f68430d763d738903feedcc4514", 
    "dest": "/tmp/hosts", 
    "gid": 0, 
    "group": "root", 
    "mode": "0644", 
    "owner": "root", 
    "path": "/tmp/hosts", 
    "size": 1036, 
    "state": "file", 
    "uid": 0
}
```
```
/opt/ansible/ansible#  ansible localhost -m copy -a "src=/tmp/new dest=/tmp/test/ group=root owner=root mode=400 backup=yes"
localhost | SUCCESS => {
    "changed": true, 
    "checksum": "da39a3ee5e6b4b0d3255bfef95601890afd80709", 
    "dest": "/tmp/test/new", 
    "gid": 0, 
    "group": "root", 
    "md5sum": "d41d8cd98f00b204e9800998ecf8427e", 
    "mode": "0400", 
    "owner": "root", 
    "size": 0, 
    "src": "/root/.ansible/tmp/ansible-tmp-1510590625.63-22887254787602/source", 
    "state": "file", 
    "uid": 0
}
