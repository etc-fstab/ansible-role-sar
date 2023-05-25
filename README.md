Role Name:
==========
This is Ansible role for managing System Activity Report. 
The role supports next use cases:

1. Define a host (use inventory_hostname) on which this role doesn't manage sar (maybe there is some reason for this).   
2. Define a host group on which this role doesn't manage sar (think of this as all hosts for a project that doesn't need sar).  
3. If there is no host or host-group based use case, then role does default sar configuration, default is based on os-family.  

Min Ansible version
-------------------
2.10.7

Requirements
------------
None

Role Variables
--------------

1. Default vars:

```sar_cfg```, ```hostgroup```

2. Host, hostgroup, os_family based vars:

```sar_package```
```sar_cron_file```
```sar_log_path```
```sar_log_path_mode```
```sar_cron_file_mode```
```sar_owner```
```sar_group```
```sar_cron_content```

Dependencies
------------
None

Example Inventory and Playbook
-----------------------------
See test folder.

Maintenance and support
-----------------------

```
1. To disable sar management by this role, in vars, create inventory_hostname.yml 
   or host-group.yml, and define sar_cfg as "No". 

2. For hostname, use Ansible var {{ inventory_hostname }}

3. If you have host/host-group based sar config, review files vars/hostname=example.yml and 
   vars/hostgroup=example.yml, and create something like that for your hosts. 
```

Author Information
------------------
ZD.

License
---------
Public domain. No ownership such as copyright, trademark, patent. No warranty.
