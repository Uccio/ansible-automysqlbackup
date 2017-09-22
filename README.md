Role Name
=========

This role installs AutoMysqlBackup on a debian system.

The original AutoMysqlBackup utility is available at https://sourceforge.net/projects/automysqlbackup/ but it does not seem to be supported at this time and there are problems with Mysql 5.6 and 5.7 so we recommend using this fork: https://github.com/sixhop/AutoMySQLBackup
The AutomysqlBackup source is configurable.

Requirements
------------

None

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

None

Example Playbook
----------------

   - hosts: mysql-servers
     become: yes
     vars_files:
       - config/automysqlbackup.yml
     roles:
       - { role: Uccio.automysqlbackup }

License
-------

GPL v3

Author Information
------------------

This role was created in 2017 by [Uccio](http://uccio.org).
