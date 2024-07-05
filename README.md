# Ansible role to configure APT
This role provides a means to configure APT on Debian and Ubuntu systems.

Requirements:

  * community.general collection

The following settings can be made with this role:

* Proxy
* Repos
* Repo keys
* Various APT settings, check defaults/main.yml

This role also provides a playbook to install a very simple proxy server, this might be expanded to have additional features later on. For now it only support setting whitelisted domains.

### Target system dependency
This role functions best if you already have python-apt installed on the target systems. If this is missing, you might run into issues when Ansible tries to configure the repositories. If the default sources file working, this role will install it automatically.
