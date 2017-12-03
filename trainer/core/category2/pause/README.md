* I'll show you how to use pause module of ansible
* Short documentation about command
```
Pauses playbook execution for a set amount of time, or until a prompt is acknowledged.
To pause/wait/sleep per host, use the wait_for module.
You can use ctrl+c if you wish to advance a pause earlier than it is set to expire or if you need to abort a playbook run entirely. To continue early press ctrl+c and then c. To abort a playbook press ctrl+c and then a.
```
* Example
```
ansible localhost -m pause -a minutes=5
Pausing for 300 seconds
(ctrl+C then 'C' = continue early, ctrl+C then 'A' = abort)
Press 'C' to continue the play or 'A' to abort 
localhost | FAILED! => {
    "failed": true, 
    "msg": "user requested abort!"
}
```
```
ansible localhost -m pause -a minutes=5
Pausing for 300 seconds
(ctrl+C then 'C' = continue early, ctrl+C then 'A' = abort)
localhost | SUCCESS => {
    "changed": false, 
    "delta": 300, 
    "failed": false, 
    "rc": 0, 
    "start": "2017-11-14 05:30:14.077795", 
    "stderr": "", 
    "stdout": "Paused for 5.0 minutes", 
    "stop": "2017-11-14 05:35:14.078019", 
    "user_input": ""
}

