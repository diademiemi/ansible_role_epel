Ansible Role EPEL
=========

[![Molecule Test](https://github.com/diademiemi/ansible_role_epel/actions/workflows/molecule.yml/badge.svg)](https://github.com/diademiemi/ansible_role_epel/actions/workflows/molecule.yml)

This is an Ansible role to install EPEL on RHEL-based systems.  
Special variables for CentOS Stream to install EPEL next are provided.  

This is mostly used in my other roles as a dependency.  

Requirements
------------
These platforms are supported:
- EL 7 (Tested on CentOS Core Linux 7)  
- EL 8 (Tested on Rocky Linux 8)  
- EL 9 (Tested on Rocky Linux 9)  

<!--
- List hardware requirements here  
-->

Role Variables
--------------

Variable | Default | Description
--- | --- | ---
<!--
`variable` | `default` | Variable example
`long_variable` | See [defaults/main.yml](./defaults/main.yml) | Variable referring to defaults
`distro_specific_variable` | See [vars/debian.yml](./vars/debian.yml) | Variable referring to distro-specific variables
-->

Dependencies
------------
<!-- List dependencies on other roles or criteria -->
None

Example Playbook
----------------

```yaml
- name: Use diademiemi.epel role
  hosts: "{{ target | default('github_cli') }}"
  roles:
    - role: "diademiemi.epel"
      tags: ['diademiemi', 'epel', 'setup']    ```

```

License
-------

MIT

Author Information
------------------

- diademiemi (@diademiemi)

Role Testing
------------

This repository comes with Molecule that run in Podman on the supported platforms.
Install Molecule by running

```bash
pip3 install -r requirements.txt
```

Run the tests with

```bash
molecule test
```

These tests are automatically ran by GitHub Actions on push. If the tests are successful, the role is automatically published to Ansible Galaxy.
