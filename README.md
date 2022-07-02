thinkpace.ansible_user
======================

This is a very simple role to create user accounts.

Role Variables
--------------

Role is using several variables which must be defined in following structure:

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

Password hash can be created with `mkpasswd --method=sha-512`. `shell` is optional, it defaults to `/bin/sh`.

See also [vars_sample.yml](vars_sample.yml).

Dependencies
------------

This role is tested on Ubuntu 20.04 (Focal Fossa).

Example Playbook
----------------

Make sure to install this role is installed before using:

`ansible-galaxy install thinkpace.ansible_user`

You can update this role with the --force flag:

`ansible-galaxy install --force thinkpace.ansible_user`

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
