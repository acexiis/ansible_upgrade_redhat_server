INFORMATION
===========
This playbook mainly work with redhat and Satellite configuration but you can easely adapt it, if you do not use Satellite.
Playbook Name
=============
  - upgrade_rhel-servers.yml

Role Name
=========

  - rhel_preupgrade
  - rhel_upgrade
  - rhel_postupgrade


Requirements
------------


Dependencies
============
Need to have a satelllite username and password with the good rights to register a server into satellite.

Variables
--------------
All those below variables have to be set and example are provide in vars_sample.yml


Example Playbook
----------------

``` ansible-playbook -i your_inventory/hosts playbooks/upgrade_rhel_server.yml ```
this playbook works with 3 main tags: 
  - preupgrade
  - upgrade
  - postupgrade
For now it's better to run this 3 tags one by one because this playbook have to reboot server
few times and the role after reboot can be ignored.

All available tags:
[delete_kernel, leapp-preupgrade, never, new_kernel, postupgrade, preupgrade, new_registration, subscription_refresh, umount, upgrade]

