logstash-indexer
========

Ansible role which installs and configures logstash-indexer.

Requirements
------------

Tested on Anbsible 1.6

Role Variables
--------------


    logstash_indexer_online_install: true                     # Whether or not to perform an online installation by downloading the installer
    logstash_indexer_installer_path: /var/logstash_indexer    # Where to find the installer for an offline installation 
    logstash_indexer_version: 1.4.0                           # The version of logstash to install
    logstash_indexer_base_install_dir: /apps                  # Where logstash will be installed
    logstash_indexer_base_logs_dir: /logs                     # Where logstash will log to
    logstash_indexer_base_data_dir: /data                     # Where logstash will store its data
    logstash_indexer_elasticsearch_cluster_members:           # Which elasticsearch members to output to
        - es1
        - es2
        - es3
    logstash_indexer_redis_hosts:                             # Which redis servers to read from
        - redis1
        - redis2
        - redis3


Dependencies
------------

None

Example Playbook
-------------------------

    - hosts: all
      sudo: yes
      roles:
         - logstash-indexer

License
-------

MIT

Author Information
------------------

Jon Hadfield
