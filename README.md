Ansible Role: Slurm
=========

An Ansible role that installs Slurm.

Requirements
------------

``` shell
# Tested software versions
$ molecule --version
molecule 6.0.2 using python 3.11 
    ansible:2.15.5
    default:6.0.2 from molecule
    docker:2.1.0 from molecule_docker requiring collections: community.docker>=3.0.2 ansible.posix>=1.4.0

# Tested distro:version
$ grep " image:" molecule/default/molecule.yml
    image: rockylinux:8.8
```

Role Variables
--------------

Here's the list of the default variables:

- slurm_version: `23.02.6`
- slurm_checksum: `sha1:3a376b165cf0ee1499ae87f5fcb4725d093c5fe7`
- slurm_prefix: `/opt/slurm-{{ slurm_version }}`
- slurm_additional_configure_options: `"--enable-pam --enable-x11"`
- slurm_install_pam_slurm_adopt: `True`
- slurm_src_install: `True`
- slurm_rpmbuild: `True`
- slurm_rpm_dir: `"{{ slurm_prefix }}/rpm"`

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
