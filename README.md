[![validation-checks](https://github.com/scottharwell/ansible_on_clouds.setup_and_config/actions/workflows/on-push.yml/badge.svg)](https://github.com/scottharwell/ansible_on_clouds.setup_and_config/actions/workflows/on-push.yml)

# Ansible on Clouds Controller Setup and Configuration

This collection contains playbooks and roles that demonstrate using configuration-as-code and gitops to declare the setup and configuration for Ansible Automation Controller.  This approach to Ansible Automation Controller configuration provides an easy-to-read and manage deployment model and keeps your Ansible Automation Controller configuration portable between different AAP deployments. 

## Included Content

<!--start collection content-->
### Roles

Click on the role name to be directed to the README specifically for that role.

| Name                                                                                                                                                  | Description                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [ansible_on_clouds.setup_and_config.azure](https://github.com/scottharwell/ansible_on_clouds.setup_and_config/blob/main/roles/azure/README.md) | Role that deploys a demo configuration of job templates, projects, inventories, etc. |

### Playbooks

| Name                                                         | Role(s) Used  | Description                                               |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------|
| `ansible_on_clouds.setup_and_config.configure_aap_azure.yml` | `roles.azure` | A playbook that runs the AAP on Azure configuration role. |

## Installation and Usage

### Installing the Collection with the Ansible Galaxy CLI

Before using the this collection, you need to install it with the Ansible Galaxy CLI:

`ansible-galaxy collection install git+https://github.com/scottharwell/ansible_on_clouds.setup_and_config.git`

You can also include it in a `requirements.yml` file and install it via `ansible-galaxy collection install -r requirements.yml`, using the format:

```yaml
---
collections:
  - name: https://github.com/scottharwell/ansible_on_clouds.setup_and_config
    type: git
    version: main
```

### Playbook Use

This collection is not available on Ansible Galaxy, so you will need to have it available for a playbook either through an Execution Environment or manual installation.  Once available, referencing the role happens just like any other Ansible role.

```yaml
- hosts: localhost
  roles:
    - role: ansible_on_clouds.setup_and_config.aoc_demo_setup
```

## License

GPLv3

## Author

This role was originally written by Scott Harwell and Hicham Mourad from the Ansible team at Red Hat.
