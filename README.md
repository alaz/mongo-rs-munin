# mongo_repl_lag

**mongo_repl_lag** is a [Munin](http://munin.projects.linpro.no/) plugin to show graphs how large the replication lag is (in seconds) per MongoDB secondary node. It requires _pymongo_ 2.4.

Configuration settings (through Munin plugin config):

* `uri` MongoDB host-port pair (optional, defaults to `localhost:27017`)
* `replicaSet` MongoDB Replica Set name
* `repl_lag.warning` warning lag (in ms)
* `repl_lag.critical` critical lag (in ms)

You are free to specify any node in a ReplicaSet, the plugin will do the rest itself.

Credits for the core algorithm are to [Nagios Munin plugin](https://github.com/mzupan/nagios-plugin-mongodb)
