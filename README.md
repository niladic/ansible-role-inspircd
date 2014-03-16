## inspircd Ansible role (FreeBSD)

This role assumes that the port irc/inspircd is already installed.

To configure inspircd.conf template, 2 variables are available: inspircd_conf and inspircd_default_conf. By default, inspircd_default_conf is filled with the exact settings in the default inspircd.conf. Each setting can be overriden by adding its key in inspircd_conf.

```
# If any of this settings are not set in inspircd_conf,
# then the template is programmed to fail:
# server, admin, binds

# A minimal inspircd_conf
inspircd_conf:
  server:
    name: penguin.omega.org.za
    description: Waddle World
    network: Omega
  admin:
    name: Johnny English
    nick: MI5
    email: MI5@the.best.secret.agent
  binds:
    - address: ""
      port: 6697
      type: clients
      ssl: gnutls
```

See defaults/main.yml and templates/inspircd.conf.j2 for documentation about the settings.
