Ansible role for deploy node-exporter packages and services. You can add custom services or packages via variables bellow.

This role is developed with Ansible 2.9.6 and tested on Ubuntu 20.04 LTS.

## Role Variables

| Variable | Required | Default | Comments |
| -------- | -------- | ------- | -------- |
| `additional_ports` | No | `{}` | Add aditional ports while using this role |

## Requirements

Ansible.posix collection

To install it, use the following command:

```yaml
ansible-galaxy collection install ansible.posix
```

## Install basic packages and services with default settings
```yaml
  roles:
     - sw-node-exporter
```

## Install basic packages and services with some custom variables
```yaml
  roles:
     - sw-node-exporter
  vars:
     - additional_ports:
        - 80/tcp
        - 443/tcp
        - 25565/udp
```


