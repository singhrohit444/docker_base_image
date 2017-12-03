* I'll show you how to use ping module of ansible
* Short documentation about command
```
A trivial test module, this module always returns pong on successful contact. It does not make sense in playbooks, but it is useful from /usr/bin/ansible to verify the ability to login and that a usable python is configured.
 - action: ping
```
* Example
```
/opt/ansible/ansible# ansible localhost -m ping
localhost | SUCCESS => {
    "changed": false, 
    "ping": "pong"
}


