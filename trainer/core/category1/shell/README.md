* I'll show you how to use shell module of ansible
* Short documentation about command
```
The shell module takes the command name followed by a list of space-delimited arguments. It is almost exactly like the command module but runs the command through a shell (/bin/sh) on the remote node.
```
* Example
```
ansible localhost -m shell -a "cat=/home/test
localhost | SUCCESS | rc=0 >>
```
```
ansible localhost -m shell -a "cp /home/test /home/ubuntu/"
localhost | SUCCESS | rc=0 >>
```

