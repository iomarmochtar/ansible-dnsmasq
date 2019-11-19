Ansible DNSMASQ Role
=====================

Ansible role for installing and configure dnsmasq service

Install
-------

Simply just use ansible-galaxy command to install

```bash
ansible-galaxy install iomarmochtar.dnsmasq
```

Role Variables
--------------

You can see all default variables in file *defaults/main.yml*, you can see in the example section for how it used.

Example Playbook
----------------

```yaml

- hosts: server
  roles:
    - role: iomarmochtar.dnsmasq
      upstreams:
        - 8.8.8.8
        - 1.1.1.1
      configs:
        - mx-host: "omar.net,smtp.omar.net,10"
        - mx-host: "mochtar.net,mx.mochtar.net,10"
        - address: "/smtp.omar.net/192.168.1.5"
        - address: "/mx.mochtar.net/192.168.1.4"
```

License
-------

GNU GPL v3.0

Author Information
------------------

```
Author: Imam Omar Mochtar
Email: iomarmochtar@gmail.com
Website: https://blog.mochtar.net
```
