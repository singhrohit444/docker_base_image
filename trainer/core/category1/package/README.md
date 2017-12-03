* I'll show you how to use package module of ansible
* Short documentation about command
```
Installs, upgrade and removes packages using the underlying OS package manager.
```
* Example
```
ansible localhost -m package -a "name=nginx state=present"
localhost | SUCCESS => {
    "cache_update_time": 1510642285, 
    "cache_updated": false, 
    "changed": true, 
    "failed": false, 
    "stderr": "", 
    "stderr_lines": [], 
    "stdout": "Reading package lists...\nBuilding dependency tree...\nReading state information...\nThe following extra packages will be installed:\n  libxslt1.1 nginx-common nginx-core\nSuggested packages:\n  fcgiwrap nginx-doc\nThe following NEW packages will be installed:\n  libxslt1.1 nginx nginx-common nginx-core\n0 upgraded, 4 newly installed, 0 to remove and 61 not upgraded.\nNeed to get 495 kB of archives.\nAfter this operation, 1802 kB of additional disk space will be used.\nGet:1 http://archive.ubuntu.com/ubuntu/ trusty-updates/main libxslt1.1 amd64 1.1.28-2ubuntu0.1 [145 kB]\nGet:2 http://archive.ubuntu.com/ubuntu/ trusty-updates/main nginx-common all 1.4.6-1ubuntu3.8 [19.1 kB]\nGet:3 http://archive.ubuntu.com/ubuntu/ trusty-updates/main nginx-core amd64 1.4.6-1ubuntu3.8 [325 kB]\nGet:4 http://archive.ubuntu.com/ubuntu/ trusty-updates/main nginx all 1.4.6-1ubuntu3.8 [5394 B]\nPreconfiguring packages ...\nFetched 495 kB in 2s (214 kB/s)\nSelecting previously unselected package libxslt1.1:amd64.\n(Reading database ... 66495 files and directories currently installed.)\nPreparing to unpack .../libxslt1.1_1.1.28-2ubuntu0.1_amd64.deb ...\nUnpacking libxslt1.1:amd64 (1.1.28-2ubuntu0.1) ...\nSelecting previously unselected package nginx-common.\nPreparing to unpack .../nginx-common_1.4.6-1ubuntu3.8_all.deb ...\nUnpacking nginx-common (1.4.6-1ubuntu3.8) ...\nSelecting previously unselected package nginx-core.\nPreparing to unpack .../nginx-core_1.4.6-1ubuntu3.8_amd64.deb ...\nUnpacking nginx-core (1.4.6-1ubuntu3.8) ...\nSelecting previously unselected package nginx.\nPreparing to unpack .../nginx_1.4.6-1ubuntu3.8_all.deb ...\nUnpacking nginx (1.4.6-1ubuntu3.8) ...\nProcessing triggers for ufw (0.34~rc-0ubuntu2) ...\nProcessing triggers for ureadahead (0.100.0-16) ...\nProcessing triggers for man-db (2.6.7.1-1ubuntu1) ...\nSetting up libxslt1.1:amd64 (1.1.28-2ubuntu0.1) ...\nSetting up nginx-common (1.4.6-1ubuntu3.8) ...\nProcessing triggers for ufw (0.34~rc-0ubuntu2) ...\nProcessing triggers for ureadahead (0.100.0-16) ...\nSetting up nginx-core (1.4.6-1ubuntu3.8) ...\nSetting up nginx (1.4.6-1ubuntu3.8) ...\nProcessing triggers for libc-bin (2.19-0ubuntu6.13) ...\n", 
    "stdout_lines": [
        "Reading package lists...", 
        "Building dependency tree...", 
        "Reading state information...", 
        "The following extra packages will be installed:", 
        "  libxslt1.1 nginx-common nginx-core", 
        "Suggested packages:", 
        "  fcgiwrap nginx-doc", 
        "The following NEW packages will be installed:", 
        "  libxslt1.1 nginx nginx-common nginx-core", 
        "0 upgraded, 4 newly installed, 0 to remove and 61 not upgraded.", 
        "Need to get 495 kB of archives.", 
        "After this operation, 1802 kB of additional disk space will be used.", 
        "Get:1 http://archive.ubuntu.com/ubuntu/ trusty-updates/main libxslt1.1 amd64 1.1.28-2ubuntu0.1 [145 kB]", 
        "Get:2 http://archive.ubuntu.com/ubuntu/ trusty-updates/main nginx-common all 1.4.6-1ubuntu3.8 [19.1 kB]", 
        "Get:3 http://archive.ubuntu.com/ubuntu/ trusty-updates/main nginx-core amd64 1.4.6-1ubuntu3.8 [325 kB]", 
        "Get:4 http://archive.ubuntu.com/ubuntu/ trusty-updates/main nginx all 1.4.6-1ubuntu3.8 [5394 B]", 
        "Preconfiguring packages ...", 
        "Fetched 495 kB in 2s (214 kB/s)", 
        "Selecting previously unselected package libxslt1.1:amd64.", 
        "(Reading database ... 66495 files and directories currently installed.)", 
        "Preparing to unpack .../libxslt1.1_1.1.28-2ubuntu0.1_amd64.deb ...", 
        "Unpacking libxslt1.1:amd64 (1.1.28-2ubuntu0.1) ...", 
        "Selecting previously unselected package nginx-common.", 
        "Preparing to unpack .../nginx-common_1.4.6-1ubuntu3.8_all.deb ...", 
        "Unpacking nginx-common (1.4.6-1ubuntu3.8) ...", 
        "Selecting previously unselected package nginx-core.", 
        "Preparing to unpack .../nginx-core_1.4.6-1ubuntu3.8_amd64.deb ...", 
        "Unpacking nginx-core (1.4.6-1ubuntu3.8) ...", 
        "Selecting previously unselected package nginx.", 
        "Preparing to unpack .../nginx_1.4.6-1ubuntu3.8_all.deb ...", 
        "Unpacking nginx (1.4.6-1ubuntu3.8) ...", 
        "Processing triggers for ufw (0.34~rc-0ubuntu2) ...", 
        "Processing triggers for ureadahead (0.100.0-16) ...", 
        "Processing triggers for man-db (2.6.7.1-1ubuntu1) ...", 
        "Setting up libxslt1.1:amd64 (1.1.28-2ubuntu0.1) ...", 
        "Setting up nginx-common (1.4.6-1ubuntu3.8) ...", 
        "Processing triggers for ufw (0.34~rc-0ubuntu2) ...", 
        "Processing triggers for ureadahead (0.100.0-16) ...", 
        "Setting up nginx-core (1.4.6-1ubuntu3.8) ...", 
        "Setting up nginx (1.4.6-1ubuntu3.8) ...", 
        "Processing triggers for libc-bin (2.19-0ubuntu6.13) ..."
    ]
}
```
```
ansible localhost -m package -a "name=nginx state=absent"
localhost | SUCCESS => {
    "changed": true, 
    "failed": false, 
    "stderr": "", 
    "stderr_lines": [], 
    "stdout": "Reading package lists...\nBuilding dependency tree...\nReading state information...\nThe following packages were automatically installed and are no longer required:\n  libxslt1.1 nginx-common nginx-core\nUse 'apt-get autoremove' to remove them.\nThe following packages will be REMOVED:\n  nginx\n0 upgraded, 0 newly installed, 1 to remove and 61 not upgraded.\nAfter this operation, 96.3 kB disk space will be freed.\n(Reading database ... 66555 files and directories currently installed.)\nRemoving nginx (1.4.6-1ubuntu3.8) ...\n", 
    "stdout_lines": [
        "Reading package lists...", 
        "Building dependency tree...", 
        "Reading state information...", 
        "The following packages were automatically installed and are no longer required:", 
        "  libxslt1.1 nginx-common nginx-core", 
        "Use 'apt-get autoremove' to remove them.", 
        "The following packages will be REMOVED:", 
        "  nginx", 
        "0 upgraded, 0 newly installed, 1 to remove and 61 not upgraded.", 
        "After this operation, 96.3 kB disk space will be freed.", 
        "(Reading database ... 66555 files and directories currently installed.)", 
        "Removing nginx (1.4.6-1ubuntu3.8) ..."
    ]
}
```
