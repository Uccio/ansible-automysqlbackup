Role Description
=========

This role installs AutoMysqlBackup on a debian system.

The original AutoMysqlBackup utility is available at https://sourceforge.net/projects/automysqlbackup/ but it does not seem to be supported at this time and there are problems with Mysql 5.6 and 5.7 so we recommend using this fork: https://github.com/sixhop/AutoMySQLBackup

The AutomysqlBackup source is configurable but all default are set to use sixhop fork.

Requirements
------------

None

Role Variables
--------------
The most important variables are:

- automysqlbackup_mysql_dump_username: Database username  that will perform the backups
- automysqlbackup_mysql_dump_password: Database password of username
- automysqlbackup_mysql_dump_host: Database host
- automysqlbackup_mysql_dump_host_friendly: Friendly name of backup files

For full list look `/defaults/main.yml` or `/templates/automysqlbackup.conf`

Dependencies
------------

None

Example Playbook
----------------
```
 - hosts: mysql-servers
   become: yes
   vars_files:
    - config/automysqlbackup.yml
      roles:
       - { role: Uccio.automysqlbackup }
```
License
-------

GPL v3

Author Information
------------------

This role was created in 2017 by [Uccio](http://uccio.org).
