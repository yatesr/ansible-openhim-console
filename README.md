Role Name
=========

ansible_openhim_console


Requirements
------------

openhim-core
Debian support only for now.

Role Variables
--------------
````
    
    # Deploy from compiled tar.gz or install from source
    openhim_console_deploy: false
    # Location of local tar.gz to deploy if above is true
    openhim_console_archive_loc:

    # Web server directory to install to
    openhim_console_web_root: /usr/share/nginx/html
    openhim_console_owner: www-data

    # Version of openhim-console to use
    openhim_console_version: 1.2.0
    openhim_console_url: "https://github.com/jembi/openhim-console/releases/download/v{{openhim_console_version}}/openhim-console-v{{openhim_console_version}}.tar.gz"
    # Git branch to install.  Leave blank to install a released version.
    openhim_console_branch:

    # Config options for default.json when using git install
    openhim_console_config_protocol: https
    openhim_console_config_host: {{ansible_default_ipv4.address}}
    openhim_console_config_port: 8080
    openhim_console_config_title: "OpenHIM Admin Console"
    openhim_console_config_footerTitle: "OpenHIM Administration Console"
    openhim_console_config_footerPoweredBy: "<a href='http://openhim.org/' target='_blank'>Powered by OpenHIM</a>"
    openhim_console_config_loginBanner:

````


Example Playbook
----------------

    - hosts: servers
      roles:
         - openhim-console
      vars:
         # Change this to the fqdn if you will access the server using its fqdn.
       	 openhim_console_config_host: {{ansible_default_ipv4.address}}

License
-------

Apache v2

Author Information
------------------

Ryan Yates
