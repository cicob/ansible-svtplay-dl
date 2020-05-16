# Introduction

Ansible-role to download and install svtplay-dl




# How to use this role

```
cat<<EOT >> requirements.yml

- src: https://github.com/cicob/ansible-svtplay-dl
  version: master
  name: cicob.ansible-svtplay-dl

EOT

ansible-galaxy install -r requirements.yml cicob.ansible-svtplay-dl

#--- to force an installation/upgrade
ansible-galaxy install -r requirements.yml --force cicob.ansible-svtplay-dl

#--- to install all and anything in the requirements.yml file (probably not what you want)
ansible-galaxy install -r requirements.yml --force
```


# Variables

  - app_user: Defaults to "ops"
  - app_group: Default to "ops"
  - usersHomeDir: Defaults to "/home"


# Example playbooks


```
---
- hosts: swedenbox
  roles:
    - cicob.ansible-svtplay-dl
  vars:
    - app_user: "vagrant"
    - app_group: "vagrant"

```



# Reference

<https://svtplay-dl.se/>

