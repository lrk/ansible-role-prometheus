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

# Prometheus system user group
prometheus_group: prometheus
# Prometheus system user name
prometheus_user: prometheus

# Prometheus install path
prometheus_path_install: /opt/prometheus
# Prometheus configuration path
prometheus_path_config: /etc/prometheus
# Prometheus logs path
prometheus_path_log:  /var/log/prometheus
# Prometheus PID path
prometheus_path_pid:  /var/run/prometheus
# Prometheus Data path:
prometheus_path_db: /var/lib/prometheus
# Prometheus rules path:
prometheus_path_rules: "{{ prometheus_path_config}}/rules"
# Prometheus file sd config path:
prometheus_path_file_sd_config: "{{ prometheus_path_config}}/tgroups"

# Prometheus components to install
# Can be a mix of:
#   - prometheus
#   - node_exporter
#   - alert_manager
prometheus_components: []


# Prometheus version
prometheus_version: 1.7.1

# Prometheus service name
prometheus_service_name: prometheus

# Address to bind on, default 0.0.0.0
prometheus_bind_address: 0.0.0.0
# Port on with prometheus will listen, default 9090
prometheus_port: 9090

# URL of alert manager service
prometheus_alertmanager_url:

#Parameters for prometheus.yml

# Scrape interval: default 15s
prometheus_scrape_interval: 15s
# Scrape timeout: default 10s
prometheus_scrape_timeout: 10s
# Evaluation interval: default 15s
prometheus_evaluation_interval: 15s

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
