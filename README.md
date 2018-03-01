Ansible Role: ucs-servers
=========

An Ansible role to perform Servers configuration on Cisco UCS Manager.

Requirements
------------

This role requires UCS modules from Ansible v2.5.
UCS Ansible modules require the ucsmsdk Python module.

Installation
------------

There are two ways you can test this role:

 1. Install it by cloning the Github repository (ensure CiscoUcs.ucs-servers is is your ANSIBLE_ROLES_PATH)

        git clone https://github.com/ciscoucs/ansible-role-ucs-servers CiscoUcs.ucs-servers

 2. Install it using the ansible-galaxy command

        ansible-galaxy install CiscoUcs.ucs-servers

Role Variables
--------------

Variables that are in defaults/main.yml are based on the FlexPod Datacenter with Docker EE Cisco Validated Design (CVD).
The Docker EE CVD is available at https://www.cisco.com/c/en/us/td/docs/unified_computing/ucs/UCS_CVDs/flexpod_docker_deploy_design.html.
Default UCS Manager login information is also provided in defaults.main.yml that can be used with the Cisco demo Cloud UCS 3.2 environment: https://dcloud-cms.cisco.com/demo/cisco-ucs-3-2-v1.

Example Playbook
----------------

tests/test.yml is an example of how to use the role:

```yaml
---
- hosts: localhost
  roles:
    - CiscoUcs.ucs-servers
```

Run the test.yml playbook with the following command:

    ansible-playbook [-i <inventory file>] test.yml

License
-------

Apache 2.0

Author Information
------------------

David Soper (@dsoper2), CiscoUcs (@CiscoUcs)
