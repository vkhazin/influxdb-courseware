# Retention Policy

* How long InfluxDB should keep data
* What number of copies to store in a cluster (not meaningful in one-node cluster)
* Time range for shard groups
* Default Retention Policy ```autogen``` is created when database is created
* ```autogen``` comes with infinite duration, a replication factor of one, and a shard group duration of seven days
* Custom retention policy can be specified when creating a database:
```
create database "fliesbees" with duration 1m replication 1 shard duration 1s name "ephemeral"
```
* A new retention policy can be created in an existing database:
```
create retention policy "ephemeral" on "fliesbees" duration 1m replication 1 default
```