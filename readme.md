##Test Server used with http clients
GET, PUT, POST or DELETE calls to {baseurl}/api/anyuri is displayed at {baseurl}

GET calls return the JSON wrapped input uri with a 200 code

PUT, POST and DELETE calls return a 201 code

All calls are Authenticated with basic http authentication


The server keep a set number of calls in it shistory and displays them oon a dynamics table.


##Dependencies

* [Scala 2.9.1](http://scala-lang.org)
* [Lift 2.4](http://liftweb.net/)


##Installation

###Development
The only prerequisite needed is [Maven](http://maven.apache.org/)

Clone this repository and run ```mvn jetty:run```

View under localhost:8080

Send input to localhost:8080/api/

 ```
 curl -v -X PUT -d '{"s":"one"}' localhost:8080/api/fopp --user simkey101:ss101 -H "Content-Type:application/json"
 ```

 ```
 curl -v -X POST -d "{"json":"test"}"  http://localhost:8080/api/testurl --user simkey101:ss101 -H "Content-Type:application/json"
 ```



###Deployment
```mvn install```

Deploy the resulting WAR file to a Servlet container like Jetty, Tomcat or Glassfish.




##License
[Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0)