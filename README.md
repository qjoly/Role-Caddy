Role Caddy
=========

Installation simple de Caddy sur une machine **Alpine**. 

Role Variables
--------------

Il faudra définir les fqdn ainsi que les IP dans le fichier `defaults/main.yml`. Le role se chargera de générer le Caddyfile
Exemple: 
```yml
caddy:
  revproxy:
  - fqdn: git.thoughtless.eu 
    url: Gitea:3000
  - fqdn: mail.thoughtless.eu
    url: 192.168.128.114:80
  - fqdn: docker.thoughtless.eu
    url: 192.168.128.81:5000
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```yml
---
- hosts: all
  remote_user: root
  roles:
    - Role-Caddy
```

License
-------

BSD
