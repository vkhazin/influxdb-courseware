# Continuous Query Lab

* Login into your sandbox instance
* Verify influxdb service is running
* Download sample data:
```
curl -O https://s3.us-east-2.amazonaws.com/tick-courseware/sample-data/NOAA_data.txt
```
* Launch <a href="https://docs.influxdata.com/influxdb/v1.3/tools/shell/" target="_blank">influxdb cli</a>
* <a href="https://docs.influxdata.com/influxdb/v1.3/query_language/database_management/#create-database" target="_blank">Create database</a> ```NOAA_water_database```
* Exit the cli
* Import the data:
```
influx -import -path=NOAA_data.txt -precision=s -database=NOAA_water_database
```
* Find the database we just created using <a href="https://docs.influxdata.com/influxdb/v1.3/query_language/schema_exploration/" target="_blank">InfluxQl</a>
* Switch to the database with ```use <db-name>``` syntax
* List measurements in the database using <a href="https://docs.influxdata.com/influxdb/v1.3/query_language/schema_exploration/" target="_blank">InfluxQl</a>
* Select data from different measurements to confirm import has been successful
* Now let's write some continuous queries