## docker

[![Ansible Galaxy](http://img.shields.io/badge/galaxy-ypid.docker-660198.svg?style=flat)](https://galaxy.ansible.com/list#/roles/4752)
[![Platforms](http://img.shields.io/badge/platforms-debian%20/%20ubuntu-lightgrey.svg?style=flat)](https://galaxy.ansible.com/list#/roles/4752)
[![GitHub Tags](https://img.shields.io/github/tag/ypid/ansible-docker.svg)](https://github.com/ypid/ansible-docker)
[![GitHub Stars](https://img.shields.io/github/stars/ypid/ansible-docker.svg)](https://github.com/ypid/ansible-docker)


Install and configure Docker.

This role installs Docker via the means of your distribution and configures it. Simple as that.

There are many Ansible roles for Docker available but most of them do some crazy stuff to get Docker up and running.
This is not necessary on up-to-date distributions anymore.

If you use [mlocate], have a look at the role [tersmitten.updatedb].

### Credits

This role reuses some templates files and variables names from [tersmitten.docker].

[mlocate]: https://packages.debian.org/search?keywords=mlocate
[tersmitten.updatedb]: https://galaxy.ansible.com/list#/roles/2463
[tersmitten.docker]: https://galaxy.ansible.com/list#/roles/2309

### Installation

This role requires at least Ansible `v1.8.4`. To install it, run:

```Shell
ansible-galaxy install ypid.docker
```

To install via git, run either:

```Shell
git clone https://github.com/ypid/ansible-docker.git ypid.docker
git submodule add https://github.com/ypid/ansible-docker.git ypid.docker
```


### Role dependencies

- `debops.apt_preferences`

### Role variables

List of default variables available in the inventory:

```YAML
---

## Customize location of Docker binary (especially for development testing).
docker_binary: ''

## Can be used to modify the daemon startup options.
docker_opts: ''
# docker_opts: '--dns {{ ansible_default_ipv4.address }}'

## If you need Docker to use an HTTP proxy, it can also be specified here.
docker_http_proxy: ''

## This is also a handy place to tweak where Docker's temporary files go.
docker_tmpdir: ''


## "Global" packages to install
docker_package_list:
  - 'docker.io'

## "Host group" packages to install
docker_package_group_list: []

## "Host" packages to install
docker_package_host_list: []
```




### Authors and license

`docker` role was written by:

- [Robin Schneider](https://github.com/ypid) | [e-mail](mailto:ypid@riseup.net)

License: [AGPLv3](https://tldrlegal.com/license/gnu-affero-general-public-license-v3-%28agpl-3.0%29)

***

README generated by [Ansigenome](https://github.com/nickjj/ansigenome/).
