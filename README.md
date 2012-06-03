# mongo_repl_lag

**mongo_repl_lag** is a [Munin](http://munin.projects.linpro.no/) plugin to show graphs how large the replication lag is (in seconds) per MongoDB secondary node. It requires _pymongo_.

Configuration settings (through Munin plugin config):

* `host` MongoDB node host (optional, defaults to `localhost`)
* `port` MongoDB node port (optional, defaults to `27017`)
* `replicaSet` MongoDB Replica Set name (optional, you would need it if **mongo_repl_lag** is installed at *arbiter* because of [PYTHON-339](https://jira.mongodb.org/browse/PYTHON-339) issue)
* `repl_lag.warning` warning lag (in ms)
* `repl_lag.critical` critical lag (in ms)

By default the plugin will connect to `localhost:27017`.

You are free to specify any node in a ReplicaSet, the plugin will do the rest itself.

Credits for the core algorithm are to [Nagios Munin plugin](https://github.com/mzupan/nagios-plugin-mongodb)
