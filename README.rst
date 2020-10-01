=====================
ROLE openshift_backup
=====================

.. image:: https://img.shields.io/github/license/adfinis-sygroup/ansible-role-openshift_backup.svg?style=flat-square
  :target: https://github.com/adfinis-sygroup/ansible-role-openshift_backup/blob/master/LICENSE

.. image:: https://img.shields.io/travis/adfinis-sygroup/ansible-role-openshift_backup.svg?style=flat-square
  :target: https://travis-ci.org/adfinis-sygroup/ansible-role-openshift_backup

.. image:: https://img.shields.io/badge/galaxy-adfinis--sygroup.openshift_backup-660198.svg?style=flat-square
  :target: https://galaxy.ansible.com/adfinis-sygroup/openshift_backup

A brief description of the role goes here.


Requirements
=============

The oc and jq binaries are required for the backup scripts. On CentOS they're
installed by the role itself.

Role Variables
===============

```
# Define the version of the OpenShift client to be installed
openshift_backup_openshift_version: "3.9"

# Contexts to be created in ~/.kube/config that will be used for backups
openshift_backup_oc_login: []

# A possible configuration could look like this:
#
# .. code-block:: YAML
#
#   openshift_backup_oc_login:
#     - server: https://openshift.example.com:443
#       token: <JWT>
```

Dependencies
=============

This role as no other dependencies.

Example Playbook
=================

.. code-block:: yaml

  - hosts: backup-server
    roles:
       - { role: adfinis-sygroup.openshift_backup }


License
========

`Apache-2.0 <https://github.com/adfinis-sygroup/ansible-role-openshift_backup/blob/master/LICENSE>`_


Author Information
===================

openshift_backup role was written by:

* Adfinis SyGroup AG | `Website <https://www.adfinis-sygroup.ch/>`_ | `Twitter <https://twitter.com/adfinissygroup>`_ | `GitHub <https://github.com/adfinis-sygroup>`_
