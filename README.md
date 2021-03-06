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
    logstash_indexer_heap_size: 2g                            # JVM heap size
    logstash_indexer_user: lsindex                            # User that will own the files and run the process
    logstash_indexer_group: lsindex                           # Group that will own the files
    logstash_indexer_redis_input_threads: 4                   # Number of redis input threads to run
    logstash_indexer_base_install_dir: /apps                  # Where logstash will be installed
    logstash_indexer_base_logs_dir: /logs                     # Where logstash will log to
    logstash_indexer_base_data_dir: /data                     # Where logstash will store its data
    logstash_indexer_redis_hosts:                             # Which redis servers to read from
        - redis1
        - redis2
        - redis3
    logstash_indexer_elasticsearch_protocol: http             # Elasticsearch server output protocol
    logstash_indexer_elasticsearch_host: es1                  # Elasticsearch server output host
    logstash_indexer_elasticsearch_port: 9200                 # Elasticsearch server output port
    logstash_indexer_java_home:                               # Specify java rather than try to detect


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
