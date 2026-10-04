# Ansible Role: HSQLDB

[![CI](https://github.com/YOUR_GITHUB_USER/ansible-role-hsqldb/actions/workflows/ci.yml/badge.svg)](https://github.com/YOUR_GITHUB_USER/ansible-role-hsqldb/actions/workflows/ci.yml)
[![Tested with Molecule](https://img.shields.io/badge/tested%20with-Molecule-2ea44f?logo=ansible&logoColor=white)](https://ansible.readthedocs.io/projects/molecule/)
[![Linted with ansible-lint](https://img.shields.io/badge/linted%20with-ansible--lint-1a1918?logo=ansible&logoColor=white)](https://ansible.readthedocs.io/projects/lint/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Ansible Galaxy](https://img.shields.io/badge/halif.hsqldb-blue?logo=ansible&logoColor=white)](https://galaxy.ansible.com/ui/standalone/roles/halif/hsqldb/)

An Ansible role that installs and configures [HSQLDB](https://hsqldb.org/) (HyperSQL Database) on Linux hosts.

## Features

- Installs the Java runtime required by HSQLDB
- Installs and configures HSQLDB
- Idempotent: a second run reports no changes
- Tested with Molecule on every push and pull request

## Requirements

- Ansible 2.14 or newer
- A target host with `systemd` and internet access to download packages

## Supported platforms

| OS     | Versions       |
|--------|----------------|
| Debian | <fill in>      |
| Ubuntu | <fill in>      |

The list must match the platforms in `molecule/default/molecule.yml` and `meta/main.yml`.

## Role variables

All variables are defined in `defaults/main.yml` and can be overridden in your playbook or inventory.

| Variable          | Default     | Description   |
|-------------------|-------------|---------------|
| `<variable_name>` | `<default>` | <description> |
| `<variable_name>` | `<default>` | <description> |

## Dependencies

None.

## Installation

From Ansible Galaxy:
```bash
ansible-galaxy role install halif.hsqldb
```

Or via `requirements.yml`:
```yaml
roles:
  - name: halif.hsqldb
```
```bash
ansible-galaxy role install -r requirements.yml
```

## Example playbook
```yaml
- name: Install HSQLDB
  hosts: db_servers
  become: true
  roles:
    - role: halif.hsqldb
      vars:
 

# &lt;variable_name&gt;: &lt;value&gt;
```

## Testing

The role is tested with [Molecule](https://ansible.readthedocs.io/projects/molecule/) using the Docker driver.
```bash
pip install ansible molecule "molecule-plugins[docker]" docker
molecule test
```

`molecule test` runs the full cycle: lint, create, prepare, converge, idempotence check, verify and destroy.

## Contributing

Issues and pull requests are welcome. Please run `ansible-lint` and `molecule test` before submitting a PR.

## License

[MIT](LICENSE)