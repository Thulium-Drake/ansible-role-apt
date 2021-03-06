[![Build Status](https://drone.element-networks.nl/api/badges/Element-Networks/ansible-role-apt/status.svg)](https://drone.element-networks.nl/Element-Networks/ansible-role-apt)

# Ansible role to configure APT
This role provides a means to configure APT on Debian and Ubuntu systems.

The following settings can be made with this role:

* Proxy
* Repos
* Repo keys
* Various APT settings, check defaults/main.yml

This role also provides a playbook to install a very simple Squid-deb-proxy server, this might be expanded to have additional features later on. For now it only support setting whitelisted domains.

## Setup
This role uses https://github.com/leapfrogonline/ansible-merge-vars/, which has to be installed on the Ansible Control Host before using this role. You need to install this plugin first, lest you get syntax errors. Installing can be done as follows:

```
pip install ansible-merge-vars
```

### Target system dependency
This role functions best if you already have python-apt installed on the target systems. If this is missing, you might run into issues when Ansible tries to configure the repositories. If the default sources file working, this role will install it automatically.
