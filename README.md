Ansible Role: Slurm
=========

An Ansible role that installs Slurm.

Requirements
------------

``` shell
# Tested software versions
$ molecule --version
molecule 5.0.1 using python 3.10 
    ansible:2.14.5
    azure:23.4.1 from molecule_plugins
    containers:23.4.1 from molecule_plugins requiring collections: ansible.posix>=1.3.0 community.docker>=1.9.1 containers.podman>=1.8.1
    delegated:5.0.1 from molecule
    docker:23.4.1 from molecule_plugins requiring collections: community.docker>=3.0.2 ansible.posix>=1.4.0
    ec2:23.4.1 from molecule_plugins
    gce:23.4.1 from molecule_plugins requiring collections: google.cloud>=1.0.2 community.crypto>=1.8.0
    podman:23.4.1 from molecule_plugins requiring collections: containers.podman>=1.7.0 ansible.posix>=1.3.0
    vagrant:23.4.1 from molecule_plugins

# Tested distro:version
$ grep " image:" molecule/default/molecule.yml
    image: rockylinux:8.7
```

Role Variables
--------------

Here's the default variables:

- slurm_version: 23.02.2
- slurm_checksum: sha1:6356bc8cb2f9d93d34c2bab1c15f2b78db4c3e6f
- slurm_prefix: /opt/slurm-{{ slurm_version }}
- slurm_additional_configure_options: "--enable-pam --enable-x11"

Visit the Slurm website if you want to use different versions (and corresponding checsums).

- https://www.schedmd.com/downloads.php

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: kojiwell.slurm

License
-------

MIT

Author Information
------------------

Created and maintained by Koji Tanaka
