# Http Api - Cont'd

* InfluxDb gets away with three response codes:
```
  2xx: E.g. 204 No Content, it was a success wirting the data
  4xx: Could not understand the request
  5xx: The system is overloaded or significantly impaired
```
* InfluxDb uses REST as a transfer protocol to InfluxDb not for the purpose of resource representation
* Sample bad request:
```
curl -i -XPOST 'http://localhost:8086/write?db=NO_SUCH_DB' \
  --data-binary 'h2o_feet,location=coyote_creek,level\ description=between\ 6\ and\ 9\ feet water_level=8.12'
```
* 404 response:
```
HTTP/1.1 404 Not Found
Content-Type: application/json
Request-Id: f7181ae3-c656-11e7-80ff-000000000000
X-Influxdb-Version: 1.3.4
Date: Fri, 10 Nov 2017 20:37:27 GMT
Content-Length: 47

{"error":"database not found: \"NO_SUCH_DB\""}
```
