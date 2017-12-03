* I'll show you how to use user  module of ansible
* Short documentation about command
```
Manage user accounts and user attributes.
```
* Example
```
ansible localhost -m user -a "name=ansible"
localhost | SUCCESS => {
    "append": false, 
    "changed": false, 
    "comment": "", 
    "failed": false, 
    "group": 1002, 
    "home": "/home/ansible", 
    "move_home": false, 
    "name": "ansible", 
    "shell": "", 
    "state": "present", 
    "uid": 1002
}
```
```
ansible localhost -m user -a "name=ansible group=ansible comment=tested-user shell=/bin/bash generate_ssh_key=yes ssh_key_bits=2048 ssh_key_file=.ssh/id_rsa"
localhost | SUCCESS => {
    "append": false, 
    "changed": false, 
    "comment": "tested-user", 
    "failed": false, 
    "group": 1002, 
    "home": "/home/ansible", 
    "move_home": false, 
    "name": "ansible", 
    "shell": "/bin/bash", 
    "ssh_fingerprint": "2048 9a:b5:65:87:db:9e:99:38:e2:29:4d:64:ec:56:ae:19  ansible-generated on vagrant-ubuntu-trusty-64 (RSA)", 
    "ssh_key_file": "/home/ansible/.ssh/id_rsa", 
    "ssh_public_key": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDEoHwThj+qk+3F4vyekccC0zrFIiW8CGFU5Gd00yEVYWpNUUm8ffxoDIPOma0uPJuABpPO8NgljJiniFanHv9Ib2ISYHX4t6L64AWFZigKShQl/PMG09aBasCtCsGJ5LExf9k7MuvkgGY4WteaZ9ND2tFwklIfGmmCQd5wNVgwC8wjtmaAIvOL/xlFpHbtzDC/capwhI+mFAP41QylceUxb9KzBAnF9dgy3RsXWqcqGMQyPKfrboVEV5nhiJHo0jJ9LLb1sV45I94FF54FuU316bbSgkZJIqbBmZoOtQnftWw3FgBLo3DHPEZr+06XN0Gyc+JYknmf9DLbriEpzz8L ansible-generated on vagrant-ubuntu-trusty-64", 
    "state": "present", 
    "uid": 1002
}
```
```
ansible localhost -m user -a "name=ansible state=absent remove=yes"
localhost | SUCCESS => {
    "changed": true, 
    "failed": false, 
    "force": false, 
    "name": "ansible", 
    "remove": true, 
    "state": "absent", 
    "stderr": "userdel: ansible mail spool (/var/mail/ansible) not found\n", 
    "stderr_lines": [
        "userdel: ansible mail spool (/var/mail/ansible) not found"
    ]
}
```
