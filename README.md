Ansible Role: netbox
=========

An Ansible role for deploying Netbox.

Role Variables
--------------

See [`defaults/main.yml`](defaults/main.yml).

External dependencies
------------

- Postgres database
- Redis
- HTTP server
- SMTP server (optional)

The Postgres database and Redis can be external.

The HTTP server (like nginx, caddy or Apache2/httpd) must be local to the Netbox installation.
See [Netbox Docs - HTTP Server](https://netboxlabs.com/docs/netbox/en/stable/installation/5-http-server/) on how to configure the web server.
Netbox is listening on the address provided in `netbox_listen_address` and contains the static files on `{{ netbox_path }}/netbox`.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: netbox
  roles:
    - role: dschemp.netbox
      become: true
```

License
-------

MIT
