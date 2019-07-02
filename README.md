Kibana
=========

Install and configure Kibana, part of the ELK stack.

Requirements
------------

None

Role Variables
--------------
These defaults are set in defaults/main.yml:

    version: 6

    configuration:
      server:
        host: "0.0.0.0"
        port: "5601"
      elasticsearch:
        url: "http://localhost:9200"

    service:
      enabled: true
      state: started

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: kibana

License
-------

MIT

Author Information
------------------

Tibor Csóka
