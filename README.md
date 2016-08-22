Ansible Role: GitKraken
=======================

[![Build Status](https://travis-ci.org/gantsign/ansible-role-gitkraken.svg?branch=master)](https://travis-ci.org/gantsign/ansible-role-gitkraken)

Role to download and install the [GitKraken](https://www.gitkraken.com) Git client.

Requirements
------------

* Ubuntu

Role Variables
--------------

The following variables will change the behavior of this role (default values
are shown below):

```yaml
# The download URL for the redistributable package
gitkraken_redis_url: https://release.gitkraken.com/linux/gitkraken-amd64.deb

# Directory to store files downloaded for GitKraken installation
gitkraken_download_dir: "{{ x_ansible_download_dir | default('~/.ansible/tmp/downloads') }}"
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - { role: gantsign.gitkraken }
```

Development & Testing
---------------------

This project uses [Molecule](http://molecule.readthedocs.io/) to aid in the
development and testing; the role is unit tested using
[Testinfra](http://testinfra.readthedocs.io/) and
[pytest](http://docs.pytest.org/).

To develop or test you'll need to have installed the following:

* Linux (e.g. [Ubuntu](http://www.ubuntu.com/))
* [Docker](https://www.docker.com/)
* [Python](https://www.python.org/) (including python-pip)
* [Ansible](https://www.ansible.com/)
* [Molecule](http://molecule.readthedocs.io/)

To run the role (i.e. the `tests/test.yml` playbook), and test the results
(`tests/test_role.py`), execute the following command from the project root
(i.e. the directory with `molecule.yml` in it):

```bash
molecule test
```

License
-------

MIT

Author Information
------------------

John Freeman

GantSign Ltd.
Company No. 06109112 (registered in England)
