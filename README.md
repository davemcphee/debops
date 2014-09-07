## phpipam

[![Travis CI](https://secure.travis-ci.org/debops/ansible-phpipam.png)](http://travis-ci.org/debops/ansible-phpipam) [![test-suite](http://img.shields.io/badge/test--suite-ansible--phpipam-blue.svg)](https://github.com/debops/test-suite/tree/master/ansible-phpipam/) [![Ansible Galaxy](http://img.shields.io/badge/galaxy-debops.phpipam-660198.svg)](https://galaxy.ansible.com/list#/roles/1586)[![Platforms](http://img.shields.io/badge/platforms-debian%20|%20ubuntu-lightgrey.svg)](#)

This role installs [phpIPAM](http://phpipam.net/), an IP Address Manager
written in PHP5. MySQL will be used as the backend database, and nginx will
be a frontend webserver.

Currently phpIPAM is deployed from DebOps repository on Github, that might be
changed in the future.

Default credentials: `Admin:ipamadmin`


### Installation

This role requires at least Ansible `v1.7.0`. To install it, run:

    ansible-galaxy install debops.phpipam



### Role dependencies

- `debops.secret`
- `debops.mysql`
- `debops.php5`
- `debops.nginx`



### Role variables

List of default variables available in the inventory:

    ---
    
    # Should phpipam role manage it's own dependencies?
    phpipam_dependencies: True
    
    # Domain on which phpIPAM is configured in nginx
    phpipam_domain: [ 'ipam.{{ ansible_domain }}' ]
    
    # phpIPAM source repository and version to deploy
    phpipam_source_address: 'https://github.com/ginas/'
    phpipam_source_repository: 'phpipam.git'
    phpipam_source_version: 'master'
    
    # phpIPAM database configuration
    phpipam_database_host: 'localhost'
    phpipam_database_user: 'phpipam'
    phpipam_database_name: 'phpipam'
    
    # List of hosts or networks in CIDR format allowed to access phpIPAM
    # If empty, allws access from all networks
    phpipam_allow: []



List of internal variables used by the role:

    phpipam_database_password


### Authors and license

`phpipam` role was written by:

- Maciej Delmanowski | [e-mail](mailto:drybjed@gmail.com) | [Twitter](https://twitter.com/drybjed) | [GitHub](https://github.com/drybjed)

License: [GPLv3](https://tldrlegal.com/license/gnu-general-public-license-v3-(gpl-3))

***

This role is part of the [DebOps](http://debops.org/) project. README generated by [ansigenome](https://github.com/nickjj/ansigenome/).
