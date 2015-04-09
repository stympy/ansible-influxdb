# InfluxDB

Install [InfluxDB](http://influxdb.org/) time series database

## Role Variables

`defaults/main.yml`

| Name                        | Default Value | Description                                                      |
|-----------------------------|---------------|------------------------------------------------------------------|
| influxdb.raft_port          | [8090]        | Port used for raft                                               |
| influxdb.replication_factor | 1             | How many servers in the cluster should have a copy of each shard |
| influxdb_client_port        | 8086          | The port for influxdb client connections                         |
| influxdb_ssl_certificate    | None          | If defined the influxdb_client_port will be set to SSL           |
| influxdb_ssl_certificate_src| None          | If defined the file at this location wil be copied to the host   |
| influxdb_use_apt            | false         | If true apt will be used to install influxdb                     |
| influxdb_deb_src_url        | http://s3.amazonaws.com/influxdb/ | If not using apt the url base to pull the deb from |

### Clustering
For influxdb 0.8.x `influxdb.seed_servers` is a list of `host:port` entries that should be set on the follower nodes.
For influxdb 0.9.x `influxdb.join_urls` is a list of `http://host:port` entries that should be set on the follower nodes.

## License

MIT
