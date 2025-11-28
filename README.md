# Ansible Logrotate
[![CI](https://github.com/supertarto/ansible-logrotate/workflows/CI/badge.svg?event=push)](https://github.com/supertarto/ansible-logrotate/actions?query=workflow%3ACI)

Install and configure logrotate with Ansible, on Debian

## Requirements
None

## Tested plateform
* Debian 12 (Bookworm)
* Debian 13 (Trixie)


## Role variables

The path of your custom scripts.
```yml
logrotate_conf_dir: "/etc/logrotate.d/"
```

List of script to remove
```yml
logrotate_scripts_to_remove: []
```

List of script to install. Path are mandatory. Remove parameters you don't use.
```yml
logrotate_scripts: []
# Exemple
#  - name: Exemple
#    paths:
#      - "/var/log/example1"
#      - "/var/log/example2"
#    frequency: "weekly"
#    keep: "52"
#    compress: true
#    delaycompress: true
#    minsize: 1M
#    maxsize: 128M
#    missingok: true
#    nomissingok: true
#    notifempty: true
#    copylog: true
#    copytruncate: true
#    create: true
#    create_mode: "0660"
#    create_user: root
#    create_group: root
#    sharedscripts: true
#    dateext: true
#    dateformat: "-%Y%m%d"
#    dateyesterday: true
#    postrotate: "systemctl restart myservice.service > /dev/null"
```

## License
GPL V3.0
