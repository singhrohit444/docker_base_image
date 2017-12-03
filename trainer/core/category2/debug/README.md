* I'll show you how to use debug  module of ansible
* Short documentation about command
```
This module prints statements during execution and can be useful for debugging variables or expressions without necessarily halting the playbook.
```
* Example
```
ansible localhost -m debug -a msg=successfull
localhost | SUCCESS => {
    "msg": "successfull"
}
```
ansible localhost -m debug -a var=result
localhost | SUCCESS => {
    "result": "VARIABLE IS NOT DEFINED!"
}
```
