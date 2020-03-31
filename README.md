clear-cache
=========

This role has objective to clear all cache profiles of F5 BIG IP LTM

Requirements
------------

Role tested in Ansible 2.9.2, Python 2.7, BIG-IP 12.1.3.5 and BIG-IP 13.1.0.1

Role Variables
--------------

defaults/main.yml:
```
- balancerName: hostname or IP Address of BIG IP Device
- balancerUser: User that have access to tmsh
- balancerPass: User password
- balancerCommands: "delete /ltm profile ramcache all" - Here is the command that clean the cache of all ram memory
```

Example Playbook
----------------

```
- name: Cleaning Cache
  hosts: your_inventory
  gather_facts: true
  connection: local
  roles:
    - clear-cache
```

License
-------

BSD

Author Information
------------------

Github: [vinealvees](#https://github.com/vinealvees/)