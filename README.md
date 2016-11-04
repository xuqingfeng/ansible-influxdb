## Ansible-Influxdb
> an ansible role to install, configure and manage [Influxdb](https://www.influxdata.com/time-series-platform/influxdb/)

[![xuqingfeng.influxdb](https://img.shields.io/badge/role-xuqingfeng.influxdb-blue.svg?style=flat-square)](https://galaxy.ansible.com/xuqingfeng/influxdb/)

### Installation

`ansible-galaxy install xuqingfeng.influxdb -p roles`

### Role Variables

```yaml
#vars/main.yml
influxdb_version: 1.0.1 #influxdb version number

#default/main.yml
#...
```

### Dependencies

### Example Playbook

```yaml
- hosts: server
  roles:
    - xuqingfeng.influxdb
```