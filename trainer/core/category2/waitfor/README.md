* I'll show you how to use waitfor module of ansible
* Short documentation about command
```
You can wait for a set amount of time timeout, this is the default if nothing is specified or just timeout is specified. This does not produce an error.
```
* Example
```
ansible localhost -m  wait_for -a timeout=30
localhost | SUCCESS => {
    "changed": false, 
    "elapsed": 30, 
    "failed": false, 
    "path": null, 
    "port": null, 
    "search_regex": null, 
    "state": "started"
}
```
```
ansible localhost -m  wait_for -a "path=/home/test state=present timeout=30"
localhost | SUCCESS => {
    "changed": false, 
    "elapsed": 0, 
    "failed": false, 
    "gid": 0, 
    "group": "root", 
    "mode": "0644", 
    "owner": "root", 
    "path": "/home/test", 
    "port": null, 
    "search_regex": null, 
    "size": 0, 
    "state": "file", 
    "uid": 0
}
```
```
ansible localhost -m  wait_for -a "path=/home/test state=absent timeout=30"
localhost | FAILED! => {
    "changed": false, 
    "elapsed": 30, 
    "failed": true, 
    "msg": "Timeout when waiting for /home/test to be absent."
}
```
```
ansible localhost -m  wait_for -a "path=/home/test search_regex=complete timeout=30"
localhost | SUCCESS => {
    "changed": false, 
    "elapsed": 0, 
    "failed": false, 
    "gid": 0, 
    "group": "root", 
    "mode": "0644", 
    "owner": "root", 
    "path": "/home/test", 
    "port": null, 
    "search_regex": "complete", 
    "size": 9, 
    "state": "file", 
    "uid": 0
}
```
