Role Name
=========

ansible_openhim_console

**WIP** Currently only deploys local archive

Requirements
------------

Debian support only for now.

Role Variables
--------------

    # Deploy from compiled tar.gz or install from source
    openhim_console_deploy: false
    # Location of local tar.gz to deploy if above is true
    openhim_console_archive_loc:

    # Web server directory to install to
    openhim_console_web_root: /usr/share/nginx/html

Example Playbook
----------------

    - hosts: servers
      roles:
         - openhim-console
      vars:
        openhim_console_web_root: /var/www/html

License
-------

Apache v2

Author Information
------------------

Ryan Yates
