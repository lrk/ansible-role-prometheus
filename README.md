Ansible Role: Prometheus ([lrk.prometheus](https://galaxy.ansible.com/lrk/prometheus/))
=========
[![Build Status](https://travis-ci.org/lrk/ansible-prometheus.svg?branch=master)](https://travis-ci.org/lrk/ansible-prometheus)

An Ansible Role that install [Prometheus](https://prometheus.io).


Supported OSes
--------------
- Centos 7

Requirements
------------

None

Role Variables
--------------

Available variables along with default values are listed below (see `defaults/main.yml`)
```yml
//TODO List available variables
prometheus_group: prometheus     #Name of the prometheus user group
prometheus_user: prometheus     #Name of the prometheus user

prometheus_path_install: /opt/prometheus    # Prometheus path for installation
prometheus_path_config: /etc/prometheus # Prometheus path for configs
prometheus_path_log:  /var/log/prometheus   # Prometheus path for logs
prometheus_path_pid:  /var/run/prometheus   # Prometheus path for PID

```

Dependencies
------------

None

Example Playbook
----------------

    TODO
    - hosts: servers
      roles:
         - lrk.prometheus


 License
 -------

 Apache License Version 2.0

 References
 ----------

- [Prometheus.io](https://prometheus.io)

Author Information
------------------
This role was created by [Lrk](https://github.com/lrk).
