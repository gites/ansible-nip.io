nip.io
========

Installs nip.io python scripts

Requirements
------------

This role requires Ansible 2.2 or higher.

Role Variables
--------------

| Name                 | Default      | Description |
|:---------------------|:-------------|:------------|
| nip_repo             | https://github.com/gites/nip.io | Repo with nip.io code |
| nip_tag              | v1.0 | Code releasea |
| nip_domains          | [ "woop.sh" ] | Domain list that will be configured in nip.io script |
| nip_dir              | /opt/nip.io | Root directory for nip.io script and config files |
| nip_ttl              | 432000 | DNS TTL
| nip_default_ipaddr   | 127.0.0.1 | |
| nip_hostmaster       | hostmaster@{{ item }} | DNS hostmaster email address, *item* is based on nip_domains list |
| nip_ns               | ns1.{{ item }} | Name server domain, *item* is based on nip_domains list |
| nip_nameservers      | [ "ns1.{{ item }}=127.0.0.1", "ns2.{{ item }}=127.0.0.1" ] | Nameservers in NS record, *item* is based on nip_domains list |

Dependencies
------------

None

Example Playbook
----------------

Installs nip.io

```yaml
- hosts: all
  roles:
    - nip.io
```

License
-------

BSD

Author Information
------------------

Gites
