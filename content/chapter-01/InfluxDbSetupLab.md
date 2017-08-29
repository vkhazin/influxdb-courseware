# InfluxDb Setup Lab

* Download and install deb package:
```
curl -O https://dl.influxdata.com/influxdb/releases/influxdb_1.3.4_amd64.deb
sudo dpkg -i influxdb_1.3.4_amd64.deb
```
* Start InfluxDb service and check status:
```
sudo systemctl start influxdb
sudo systemctl status influxdb
```
* Expected Output:
```
influxdb.service - InfluxDB is an open-source, distributed, time series database
   Loaded: loaded (/lib/systemd/system/influxdb.service; enabled; vendor preset: enabled)
   Active: active (running) since Mon 2017-08-28 21:04:51 UTC; 28min ago
     Docs: https://docs.influxdata.com/influxdb/
 Main PID: 2690 (influxd)
    Tasks: 10
   Memory: 12.5M
      CPU: 5.962s
   CGroup: /system.slice/influxdb.service
           └─2690 /usr/bin/influxd -config /etc/influxdb/influxdb.conf 
````
* 