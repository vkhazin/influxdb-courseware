# Node.js Client Library Lab

* Login into your sandbox instance
* Install Node.Js and package manager npm:
```
sudo apt-get install nodejs npm -y
```
* Check Node.Js and Npm have been installed 
```
npm --version
nodejs --version
```
* Create new folder for the project: ```mkdir ./nodejs-influxdb-sample```
* Initialize the project:
```
cd nodejs-influxdb-sample/
npm init
```
* Install client library:
```
npm install --save influx
```
* Create index.js file:
```
nano ./index.js
```
* Copy-paste start of the program:
```
const Influx = require('influx')
const client = new Influx.InfluxDB({
  host: 'localhost',
  database: 'NOAA_water_database',
  schema: [
    {
      measurement: 'h2o_feet',
      fields: {
        water_level: Influx.FieldType.FLOAT
      },
      tags: [
        'location',
        'level description'
      ]
    }
  ]
});
```
