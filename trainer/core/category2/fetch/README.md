* I'll show you how to use fetch module of ansible
* Short documentation about command
```
This module works like copy, but in reverse. It is used for fetching files from remote machines and storing them locally in a file tree.
```
* Example
```
ansible localhost -m fetch -a "src=/etc/ansible/hosts dest=/home/vagrant/ flat=yes"

localhost | SUCCESS => {
    "changed": true, 
    "checksum": "da996f1a52dbae3b6b43a6c50d761e4ed5ec9a9f", 
    "dest": "/home/vagrant/hosts", 
    "failed": false, 
    "md5sum": "1564b951dc7c8511c6f9ee842653c541", 
    "remote_checksum": "da996f1a52dbae3b6b43a6c50d761e4ed5ec9a9f", 
    "remote_md5sum": null
}
```
```
ansible localhost -m fetch -a "src=/etc/ansible/new dest=/home/vagrant/ fail_on_missing=yes flat=yes"
localhost | FAILED! => {
    "changed": false, 
    "failed": true, 
    "msg": "file not found: /etc/ansible/new"
}
```
```
ansible localhost -m fetch -a "src=/etc/ansible/new dest=/home/vagrant/ fail_on_missing=no flat=yes"
localhost | SUCCESS => {
    "changed": false, 
    "failed": false, 
    "file": "/etc/ansible/new", 
    "msg": "the remote file does not exist, not transferring, ignored"
}
```

