Kibana
=========

Install and configure Kibana, part of the ELK stack.

Requirements
------------

None

Role Variables
--------------
These variables are defined in [defaults/main.yml](./defaults/main.yml):

    elk_version: 6

    elk_kibana_service:
      enabled: true
      state: started

These variables can further be set:

    elk_kibana_configuration:       # the entire kibana configuration in YAML format

Dependencies
------------

None

Example Playbook
----------------

    - name: Converge
      hosts: all
      roles:
        - role: kibana
          vars:
            elk_kibana_configuration:
              server:
                host: "0.0.0.0"
                port: "5601"
              elasticsearch:
                url: "http://localhost:9200"

License
-------

MIT

Author Information
------------------

Tibor Csóka
