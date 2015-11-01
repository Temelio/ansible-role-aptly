aptly
=====

[![Build Status](https://travis-ci.org/infOpen/ansible-role-aptly.svg?branch=master)](https://travis-ci.org/infOpen/ansible-role-aptly)

Install aptly package.

Requirements
------------

This role requires Ansible 1.5 or higher, and platform requirements are listed
in the metadata file.

User should have a custom GPG key, not automatic creation

Testing
-------

This role has two test methods :

- localy with Vagrant :
    vagrant up

- automaticaly by Travis

To not have a fake gpg key used only for tests, i've add tags for tasks about
gpg.
These tasks are skipped for Travis tests, but can be tested by Vagrant with
proper environment variables :
- APTLY_CUSTOM_GPG_KEY_FILE
- APTLY_CUSTOM_GPG_KEY_ID

Vagrant should be used to check the role before push changes to Github.

Role Variables
--------------

Follow the possible variables with their default values

Specific OS family vars :

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: achaussier.aptly }

License
-------

MIT

Author Information
------------------

Alexandre Chaussier (for Infopen company)
- http://www.infopen.pro
- a.chaussier [at] infopen.pro } }}"

