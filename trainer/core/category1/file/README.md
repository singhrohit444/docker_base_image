* I'll show you how to use file module of ansible
* Short documentation about command
```
The file module allows changing ownership and permissions on files. These same options can be passed directly to the copy module as well.
```
* Example
```
ansible localhost -m file -a "dest=/opt/ mode=600"
localhost | SUCCESS => {
    "changed": true, 
    "gid": 0, 
    "group": "root", 
    "mode": "0600", 
    "owner": "root", 
    "path": "/opt/", 
    "size": 4096, 
    "state": "directory", 
    "uid": 0
}
```
```
The file module can also create directories, similar to mkdir -p.
ansible localhost -m file -a "dest=/tmp/file mode=755 owner=root group=root state=directory"
localhost | SUCCESS => {
    "changed": true, 
    "gid": 0, 
    "group": "root", 
    "mode": "0755", 
    "owner": "root", 
    "path": "/tmp/file", 
    "size": 4096, 
    "state": "directory", 
    "uid": 0
}
```
```
ansible localhost -m file -a "dest=/tmp/file mode=755 owner=root group=root state=absent"
localhost | SUCCESS => {
    "changed": true, 
    "path": "/tmp/file", 
    "state": "absent"
}
```
```
The file module can also create directories, similar to touch file.
ansible localhost -m file -a "dest=/tmp/file mode=755 owner=root group=root state=touch"
localhost | SUCCESS => {
    "changed": true, 
    "dest": "/tmp/file", 
    "gid": 0, 
    "group": "root", 
    "mode": "0755", 
    "owner": "root", 
    "size": 0, 
    "state": "file", 
    "uid": 0
}

