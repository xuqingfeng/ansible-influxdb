## Ansible-Influxdb
> an ansible role to install, configure and manage [Influxdb](https://www.influxdata.com/time-series-platform/influxdb/)

[![xuqingfeng.influxdb](https://img.shields.io/badge/role-xuqingfeng.influxdb-blue.svg?style=flat-square)](https://galaxy.ansible.com/xuqingfeng/influxdb/)

### Installation

`ansible-galaxy install xuqingfeng.influxdb -p roles`

### Role Variables

```yaml
#vars/main.yml
influxdb_version: 1.1.1 #influxdb version number; get from https://www.influxdata.com/downloads/

#default/main.yml
#...
```

### Example Playbook

```yaml
- hosts: server
  roles:
    - xuqingfeng.influxdb
```

### Docker 

[https://github.com/influxdata/influxdata-docker/tree/master/influxdb](https://github.com/influxdata/influxdata-docker/tree/master/influxdb)