* View module types
```
/opt/ansible/ansible/lib/ansible/modules# tree -L 2
.
|-- __init__.py
|-- __init__.pyc
|-- core
|   |-- CONTRIBUTING.md
|   |-- COPYING
|   |-- README.md
|   |-- VERSION
|   |-- __init__.py
|   |-- cloud
|   |-- commands
|   |-- database
|   |-- files
|   |-- inventory
|   |-- network
|   |-- packaging
|   |-- source_control
|   |-- system
|   |-- test
|   |-- test-docs.sh
|   |-- test-requirements.txt
|   |-- utilities
|   |-- web_infrastructure
|   `-- windows
`-- extras
    |-- CONTRIBUTING.md
    |-- COPYING
    |-- README.md
    |-- REVIEWERS.md
    |-- VERSION
    |-- __init__.py
    |-- cloud
    |-- clustering
    |-- commands
    |-- database
    |-- files
    |-- messaging
    |-- monitoring
    |-- network
    |-- notification
    |-- packaging
    |-- source_control
    |-- system
    |-- test-docs.sh
    |-- web_infrastructure
    `-- windows
```
* Core modules
```
/opt/ansible/ansible/lib/ansible/modules/core# ls -d */
cloud/     database/  inventory/  packaging/       system/  utilities/           windows/
commands/  files/     network/    source_control/  test/    web_infrastructure/
```
* Extra modules
```
/opt/ansible/ansible/lib/ansible/modules/extras# ls -d */
cloud/       database/   monitoring/    packaging/       web_infrastructure/
clustering/  files/      network/       source_control/  windows/
commands/    messaging/  notification/  system/
```
