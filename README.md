# Install nginx with Ansible

[![Build Status](https://travis-ci.org/morbidick/ansible-role-nginx.svg?branch=master)](https://travis-ci.org/morbidick/ansible-role-nginx)

Very basic nginx installation with best practices concerning SSL/TLS and global Let's Encrypt, doesn't manage certs and vhosts therefore see [certbot](https://github.com/morbidick/ansible-role-certbot) and [nginx role](https://github.com/morbidick/ansible-role-nginx).

See [the full example](https://github.com/morbidick/ansible-role-nginx-vhosts/blob/master/webserver.md) for a complete playbook.

## TODO
* use pregenerated dhparams https://wiki.mozilla.org/Security/Server_Side_TLS#Pre-defined_DHE_groups

## Requirements

None.

## Example playbook

````yaml
- hosts: all
  become: yes

  roles:
  - nginx
````

## Role variables

None of the variables below are required.

| Variable                 | Default   | Comment |
| :---                     | :---      | :---    |

For all options see [defaults/main.yml](defaults/main.yml)

## Development

You can use the [Vagrantfile](Vagrantfile) for local testing, just install vagrant and virtualbox and execute the following commands:

````bash
vagrant up
vagrant provision
````

## License

MIT
