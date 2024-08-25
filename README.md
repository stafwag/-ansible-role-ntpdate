# Ansible Role: ntpdate

An Ansible role to activate the ntpdate service on FreeBSD and NetBSD.

# Installation

## Ansible galaxy

The role is available on [Ansible Galaxy](https://galaxy.ansible.com/ui/standalone/roles/stafwag/ntpd/).

To install the role from Ansible Galaxy execute the command below. 

```bash
ansible-galaxy install stafwag.ntpdate
```
## Source Code

If you want to use the source code directly.

Clone the role source code.

```bash
$ git clone https://github.com/stafwag/ansible-role-ntpdate
```

and put into the [role search path](https://docs.ansible.com/ansible/2.4/playbooks_reuse_roles.html#role-search-path)

## Requirements

### Supported platforms

* FreeBSD
* NetBSD

## Dependencies

None

## Example Playbooks

```
- name: Configure ntp on the systems
  hosts: all
  become: true
  roles:
    - stafwag.ntpdate
    - stafwag.ntpd
  vars:
    ntpd:
      servers:
        - 0.be.pool.ntp.org
        - 1.be.pool.ntp.org
        - 2.be.pool.ntp.org
        - 3.be.pool.ntp.org
```

## License

MIT/BSD

## Author Information

Created by Staf Wagemakers, email: staf@wagemakers.be, personal website: https://www.wagemakers.be, my company https://mask27.dev
