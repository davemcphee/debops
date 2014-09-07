## java

[![Travis CI](https://secure.travis-ci.org/debops/ansible-java.png)](http://travis-ci.org/debops/ansible-java) [![test-suite](http://img.shields.io/badge/test--suite-ansible--java-blue.svg)](https://github.com/debops/test-suite/tree/master/ansible-java/) [![Ansible Galaxy](http://img.shields.io/badge/galaxy-debops.java-660198.svg)](https://galaxy.ansible.com/list#/roles/1571)[![Platforms](http://img.shields.io/badge/platforms-debian%20|%20ubuntu-lightgrey.svg)](#)

This role installs OpenJDK Java packages. It is useful as a dependency of
other roles.


### Installation

This role requires at least Ansible `v1.7.0`. To install it, run:

    ansible-galaxy install debops.java






### Role variables

List of default variables available in the inventory:

    ---
    
    # Available options for installing Java Open JDK:
    #   7-jre
    #   6-jre
    #   7-jdk
    #   6-jdk
    java_versions:
      - '7-jre'




### Authors and license

`java` role was written by:

- Nick Janetakis | [e-mail](mailto:nick.janetakis@gmail.com) | [Twitter](https://twitter.com/nickjanetakis) | [GitHub](https://github.com/nickjj)

License: [GPLv3](https://tldrlegal.com/license/gnu-general-public-license-v3-(gpl-3))

***

This role is part of the [DebOps](http://debops.org/) project. README generated by [ansigenome](https://github.com/nickjj/ansigenome/).
