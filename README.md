InfluxDB
========

Install [InfluxDB](http://influxdb.org/) time series database

Role Variables
--------------

`defaults/main.yml`

| Name                        | Default Value | Description                                                      |
|-----------------------------|---------------|------------------------------------------------------------------|
| influxdb.version            | 0.5.4         | Version to install                                               |
| influxdb.raft_port          | [8090]        | Port used for raft                                               |
| influxdb.seed_servers       | []            | List of host:port to use as cluster seed servers                 |
| influxdb.replication_factor | 1             | How many servers in the cluster should have a copy of each shard |
| influxdb_client_port        | 8086          | The port for influxdb client connections                         |
| influxdb_ssl_certificate    | None          | If defined the influxdb_client_port will be set to SSL           |
| influxdb_ssl_certificate_src| None          | If defined the file at this location wil be copied to the host   |


Example Playbook
-------------------------

    - hosts: servers
      roles:
         - stympy.influxdb

License
-------

MIT

Author Information
------------------

Benjamin Curtis <benjamin.curtis@gmail.com>
