cisco_asa_backup_config
=========

A role that creates backups of configurations in a Cisco ASA.
The role works with ASAs both with and without security contexts.

Requirements
------------

This role requires the [asa command module](https://docs.ansible.com/ansible/latest/collections/cisco/asa/asa_command_module.html).
It can be installed by ```ansible-galaxy collection install cisco.asa```

Role Variables
--------------

### backup_destination:
This option provides the path ending with directory name in which the backup configuration file(s) will be stored. If the directory does not exist it will be first created.
If the variable is not given a backup directory named ```backup``` will be created in the current working directory and backups will be copied to that directory.


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

- hosts: all
  gather_facts: no
  roles:
    - cisco_asa_backup_config

  vars:
    backup_destination: /tmp/asa_backups/



License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
