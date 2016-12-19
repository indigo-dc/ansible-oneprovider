Oneprovider 
=========

Oneprovider is a main data management component of Onedata, designed to be deployed at each storage provider site, responsible for unifying and controlling access to data over low level storage resources of the provider,

You can use this Ansible role to install Oneprovider on a single machine. Furthermore this role allows you to
- check if machine meets minimal hardware req., needed ports are open and FQDN is properly resolved
- install, configure and uninstall Oneprovider
- uninstall Oneprovider
- stop Oneprovider services

Requirements
------------

This role requires version Ansible 2.2.0 or newer.

Role Variables
--------------

This role does not include variables that user need to define prior to using the role. All variables that might be of interest are located and documented in: defaults/main.yml

Dependencies
------------

This role has no dependencies.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

~~~
- hosts: all
  become: yes
  
  roles:
    - { role: onedata.oneprovider, requirements_check: true, oneprovider_install: true, oneprovider_configure: true, oneprovider_restart: true, oneprovider_uninstall: true} # This illustrates all possible stages that can be run with this playbook
    # - { role: onedata.oneprovider } # by default only options oneprovider_configure and oneprovider_install will run, if no options are specified
~~~

License
-------

MIT