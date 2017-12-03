* I'll show you how to use setup module of ansible
* Short documentation about command
```
name: Gathers   facts   a bout   remot e   hosts
  action: setup
      fact_path              # path used for local ansible facts (*.fact) - files in this dir will be run (if executable) and their results be added to ansible_local facts if a file is not executable it is read. File/results format can be json or ini-format
      filter                 # if supplied, only return facts that match this shell-style (fnmatch) wildcard.
```
* Example
```
/opt/ansible/ansible# ansible localhost -m setup
localhost | SUCCESS => {
    "ansible_facts": {
        "ansible_all_ipv4_addresses": [
            "172.17.0.3"
        ],
        "ansible_all_ipv6_addresses": [
            "fe80::42:acff:fe11:3"
        ],
        "ansible_architecture": "x86_64",
        "ansible_bios_date": "03/14/2014",
        "ansible_bios_version": "1.00",
        "ansible_cmdline": {
            "com.docker.database": "com.docker.driver.amd64-linux",
            "com.docker.driver": "com.docker.driver.amd64-linux,",
            "console": "ttyS0",
            "earlyprintk": "serial",
            "mobyplatform": "mac",
            "ntp": "gateway",
            "page_poison": "1",
            "panic": "1",
            "vsyscall": "emulate"
        },
        "ansible_date_time": {
            "date": "2017-11-13",
            "day": "13",
            "epoch": "1510585542",
            "hour": "15",
            "iso8601": "2017-11-13T15:05:42Z",
            "iso8601_basic": "20171113T150542832210",
            "iso8601_basic_short": "20171113T150542",
            "iso8601_micro": "2017-11-13T15:05:42.832272Z",
            "minute": "05",
            "month": "11",
            "second": "42",
            "time": "15:05:42",
            "tz": "UTC",
            "tz_offset": "+0000",
            "weekday": "Monday",
            "weekday_number": "1",
            "weeknumber": "46",
            "year": "2017"
        },
        "ansible_default_ipv4": {
            "address": "172.17.0.3",
            "alias": "eth0",
            "broadcast": "global",
            "gateway": "172.17.0.1",
            "interface": "eth0",
            "macaddress": "02:42:ac:11:00:03",
            "mtu": 1500,
            "netmask": "255.255.0.0",
            "network": "172.17.0.0",
            "type": "ether"
        },
        "ansible_default_ipv6": {},
        "ansible_devices": {
            "sda": {
                "holders": [],
                "host": "",
                "model": "BHYVE SATA DISK",
                "partitions": {
                    "sda1": {
                        "sectors": "134215680",
                        "sectorsize": 512,
                        "size": "64.00 GB",
                        "start": "2048"
                    }
                },
                "removable": "0",
                "rotational": "1",
                "scheduler_mode": "deadline",
                "sectors": "134217728",
                "sectorsize": "512",
                "size": "64.00 GB",
                "support_discard": "512",
                "vendor": "ATA"
            }
        },
        "ansible_distribution": "Ubuntu",
        "ansible_distribution_major_version": "14",
        "ansible_distribution_release": "trusty",
        "ansible_distribution_version": "14.04",
        "ansible_dns": {
            "nameservers": [
                "192.168.65.1"
            ]
        },
        "ansible_domain": "",
        "ansible_env": {
            "HOME": "/root",
            "LANG": "C",
            "LC_ALL": "C",
            "LC_MESSAGES": "C",
            "LOGNAME": "root",
            "MAIL": "/var/mail/root",
            "PATH": "/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games",
            "PWD": "/root",
            "SHELL": "/bin/bash",
            "SHLVL": "1",
            "SSH_CLIENT": "::1 40208 22",
            "SSH_CONNECTION": "::1 40208 ::1 22",
            "SSH_TTY": "/dev/pts/1",
            "TERM": "xterm",
            "USER": "root",
            "_": "/usr/bin/python"
        },
        "ansible_eth0": {
            "active": true,
            "device": "eth0",
            "ipv4": {
                "address": "172.17.0.3",
                "broadcast": "global",
                "netmask": "255.255.0.0",
                "network": "172.17.0.0"
            },
            "ipv6": [
                {
                    "address": "fe80::42:acff:fe11:3",
                    "prefix": "64",
                    "scope": "link"
                }
            ],
            "macaddress": "02:42:ac:11:00:03",
            "mtu": 1500,
            "promisc": false,
            "type": "ether"
        },
        "ansible_fips": false,
        "ansible_form_factor": "Unknown",
        "ansible_fqdn": "cf8921844585",
        "ansible_gre0": {
            "active": false,
            "device": "gre0",
            "macaddress": "00:00:00:00",
            "mtu": 1476,
            "promisc": false
        },
        "ansible_gretap0": {
            "active": false,
            "device": "gretap0",
            "mtu": 1462,
            "promisc": false,
            "type": "ether"
        },
        "ansible_hostname": "cf8921844585",
        "ansible_interfaces": [
            "gre0",
            "ip6tnl0",
            "lo",
            "tunl0",
            "ip6_vti0",
            "gretap0",
            "sit0",
            "ip6gre0",
            "ip_vti0",
            "eth0"
        ],
        "ansible_ip6_vti0": {
            "active": false,
            "device": "ip6_vti0",
            "macaddress": "00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00",
            "mtu": 1500,
            "promisc": false
        },
        "ansible_ip6gre0": {
            "active": false,
            "device": "ip6gre0",
            "macaddress": "00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00",
            "mtu": 1448,
            "promisc": false
        },
        "ansible_ip6tnl0": {
            "active": false,
            "device": "ip6tnl0",
            "macaddress": "00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00",
            "mtu": 1452,
            "promisc": false
        },
        "ansible_ip_vti0": {
            "active": false,
            "device": "ip_vti0",
            "macaddress": "00:00:00:00",
            "mtu": 1332,
            "promisc": false
        },
        "ansible_kernel": "4.9.13-moby",
        "ansible_lo": {
            "active": true,
            "device": "lo",
            "ipv4": {
                "address": "127.0.0.1",
                "broadcast": "host",
                "netmask": "255.0.0.0",
                "network": "127.0.0.0"
            },
            "ipv6": [
                {
                    "address": "::1",
                    "prefix": "128",
                    "scope": "host"
                }
            ],
            "mtu": 65536,
            "promisc": false,
            "type": "loopback"
        },
        "ansible_lsb": {
            "codename": "trusty",
            "description": "Ubuntu 14.04.3 LTS",
            "id": "Ubuntu",
            "major_release": "14",
            "release": "14.04"
        },
        "ansible_machine": "x86_64",
        "ansible_memfree_mb": 1569,
        "ansible_memory_mb": {
            "nocache": {
                "free": 1819,
                "used": 179
            },
            "real": {
                "free": 1569,
                "total": 1998,
                "used": 429
            },
            "swap": {
                "cached": 0,
                "free": 1023,
                "total": 1023,
                "used": 0
            }
        },
        "ansible_memtotal_mb": 1998,
        "ansible_mounts": [
            {
                "device": "/dev/sda1",
                "fstype": "ext4",
                "mount": "/etc/resolv.conf",
                "options": "rw,relatime,data=ordered",
                "size_available": 55041093632,
                "size_total": 67371577344,
                "uuid": "NA"
            },
            {
                "device": "/dev/sda1",
                "fstype": "ext4",
                "mount": "/etc/hostname",
                "options": "rw,relatime,data=ordered",
                "size_available": 55041093632,
                "size_total": 67371577344,
                "uuid": "NA"
            },
            {
                "device": "/dev/sda1",
                "fstype": "ext4",
                "mount": "/etc/hosts",
                "options": "rw,relatime,data=ordered",
                "size_available": 55041093632,
                "size_total": 67371577344,
                "uuid": "NA"
            }
        ],
        "ansible_nodename": "cf8921844585",
        "ansible_os_family": "Debian",
        "ansible_pkg_mgr": "apt",
        "ansible_processor": [
            "GenuineIntel",
            "Intel(R) Core(TM) i7-4870HQ CPU @ 2.50GHz",
            "GenuineIntel",
            "Intel(R) Core(TM) i7-4870HQ CPU @ 2.50GHz",
            "GenuineIntel",
            "Intel(R) Core(TM) i7-4870HQ CPU @ 2.50GHz",
            "GenuineIntel",
            "Intel(R) Core(TM) i7-4870HQ CPU @ 2.50GHz"
        ],
        "ansible_processor_cores": 1,
        "ansible_processor_count": 4,
        "ansible_processor_threads_per_core": 1,
        "ansible_processor_vcpus": 4,
        "ansible_product_name": "BHYVE",
        "ansible_product_serial": "None",
        "ansible_product_uuid": "A29F0F43-6C26-C938-88B4-419681A11408",
        "ansible_product_version": "1.0",
        "ansible_python_version": "2.7.6",
        "ansible_selinux": false,
        "ansible_sit0": {
            "active": false,
            "device": "sit0",
            "macaddress": "00:00:00:00",
            "mtu": 1480,
            "promisc": false
        },
        "ansible_ssh_host_key_dsa_public": "AAAAB3NzaC1kc3MAAACBAPsmijJxLyQJTapJO06ae/JxvKiUSzOfL2NHnxu+nhH+nDTxrVXZ3cYLVOrRZ0vdPr2++02SnNMCzipZABwWqYWrAuGBjypzAb0pIE1xVm6wJHiUlf9DVmVM/BRyBIF/XZo7pEOxzlsovBFc60Capa2d3K3f6OkCTFDD1Z6sQUYZAAAAFQDqkaVjA8KIU6TGpcKfGSk4YA88QwAAAIEAmagNfIt9FADiclgIqHx4+MzplwP/7IF5507jOZnD/Hn5MASDXTMK0MJ5eSDBh/323jb4/EF3Sf75DTUMz153AUAMZzt6/SJGY7f1M3KdVu5ujzp7t84m0Q/G7k48tB7muqSmTEHwzvvkSxAT3Duknmp3sIbT0TQd6toOfd37t68AAACBAO6tOtW6UjR6XmWxnkA8rrpMuiXblvzHeos6Oy4YypGalAW+tiaV7I8kNE4t8Gwb618899KInHUjL4nWoEzqbdV8hBs6kVOv2NKBEm2y1AEO4PO4JlVd7xFutTrcAB4HkjpYl2gDFBNDG+F9riq8dwcXKv63HEOxlYTU8ooKf7r/",
        "ansible_ssh_host_key_ecdsa_public": "AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBD8oEqutWUdLFO9Aj6lT6aBvSmqWdK8rUzqGBhI9NcAdv0nbnfVpY9Q+UwXU6xHkXvoLv7ywe3S0dNe0RxQsmdw=",
        "ansible_ssh_host_key_ed25519_public": "AAAAC3NzaC1lZDI1NTE5AAAAICTr0VLKdXE+kWdoxk8WOaqRq2od/0r5tWHkM5rLLHjr",
        "ansible_ssh_host_key_rsa_public": "AAAAB3NzaC1yc2EAAAADAQABAAABAQC7ffWyXG4/a+B6lxyF2t2kwAuCE1/VOyOhlmwljgjW6eg7FhI5sddcRRBfaOabATdJO4rVQ/Er2hHSJhnCUYi0X93wTAuC1d/dJxIjjoLxE+nTnI4nzFpfU1vKXbNH3PZIvEg0xG+ljxonZclkm/B82xltg5xVyGUReyXznv2jYQyeIS/bDU4cVR2mYVDQQbXEYajp4zDaMeo2a7ovtoHn0hy0a4mD/oZTnGYUhGRIyV/U8INtb0pg07douo4rXIavznZfYzmFg8JXXSgQajKw8RRPSXmgmLpzor0wsWFP5vRryA6ahsH6YZSqW4PN2QXVvreXd9Rxf/MowtIBYnMf",
        "ansible_swapfree_mb": 1023,
        "ansible_swaptotal_mb": 1023,
        "ansible_system": "Linux",
        "ansible_system_vendor": "NA",
        "ansible_tunl0": {
            "active": false,
            "device": "tunl0",
            "macaddress": "00:00:00:00",
            "mtu": 1480,
            "promisc": false
        },
        "ansible_uptime_seconds": 3692,
        "ansible_user_dir": "/root",
        "ansible_user_gecos": "root",
        "ansible_user_gid": 0,
        "ansible_user_id": "root",
        "ansible_user_shell": "/bin/bash",
        "ansible_user_uid": 0,
        "ansible_userspace_architecture": "x86_64",
        "ansible_userspace_bits": "64",
        "ansible_virtualization_role": "guest",
        "ansible_virtualization_type": "docker",
        "module_setup": true
    },
    "changed": false
}
```
```
ansible localhost -m setup -a "filter=ansible_user*"
localhost | SUCCESS => {
    "ansible_facts": {
        "ansible_user_dir": "/root",
        "ansible_user_gecos": "root",
        "ansible_user_gid": 0,
        "ansible_user_id": "root",
        "ansible_user_shell": "/bin/bash",
        "ansible_user_uid": 0,
        "ansible_userspace_architecture": "x86_64",
        "ansible_userspace_bits": "64"
    },
    "changed": false
}
```
```
ansible localhost -m setup -a 'filter=ansible_eth[0-2]'
localhost | SUCCESS => {
    "ansible_facts": {
        "ansible_eth0": {
            "active": true,
            "device": "eth0",
            "ipv4": {
                "address": "172.17.0.3",
                "broadcast": "global",
                "netmask": "255.255.0.0",
                "network": "172.17.0.0"
            },
            "ipv6": [
                {
                    "address": "fe80::42:acff:fe11:3",
                    "prefix": "64",
                    "scope": "link"
                }
            ],
            "macaddress": "02:42:ac:11:00:03",
            "mtu": 1500,
            "promisc": false, 
            "type": "ether"
        }
    },
    "changed": false
}
```
