thinkpace.ansible_user
=========

This is a very simple role to create user accounts.

Role Variables
--------------

Role is using existing host variables for respective server which must be defined like that:

```
os:
  users:
    - user1:
       username: "user1"
       password: PASSWORDHASH
       shell: "/bin/bash"
     - user2:
       username: "tobias"
       password: PASSWORDHASH
```

Password hash can be created with `mkpasswd --method=sha-512`. Shell is optional, it defaults to `/bin/sh`.

Example Playbook
----------------

This role can be used like following:

```
    - hosts: servers
      roles:
         - { role: thinkpace.ansible_user }
```

License
-------

GNU Affero General Public License v3.0

Author Information
------------------

[Tobias Baus](https://tobiasbaus.de)
