## What's Continuous Integration?


##  CONTINUOUS INTEGRATION

* Continuous integration (CI) is the practice of merging all developer working copies to a shared mainline several times a day.


##  CONTINUOUS INTEGRATION

* Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

 ![git](https://blog.cpanel.com/wp-content/uploads/2018/05/image2018-2-8_17-46-1.png?raw=true) 


##  CONTINUOUS INTEGRATION

* Then... we have code and branches, now what?

![jackie](./img/Jackie-chan-confused.png?raw=true) 


##  CONTINUOUS INTEGRATION

* let's build, but... what it's a build?


##  CONTINUOUS INTEGRATION

* In the field of software development, the term build is similar to that of any other field.That is, the construction of something that has an observable and tangible result.


##  CONTINUOUS INTEGRATION

* Build automation is the process of automating the creation of a software build and the associated processes including: compiling computer source code into binary code, packaging binary code, and running automated tests.


##  CONTINUOUS INTEGRATION

 ![maven](./img/maven-logo.png?raw=true) 
 ![gradle](./img/gradle.png?raw=true) 
 ![ant](./img/ant.png?raw=true) 


##  CONTINUOUS INTEGRATION

* ok, we did a Build and now what????

![jackie](./img/Jackie-chan-confused.png?raw=true) 


##  CONTINUOUS INTEGRATION

* Now we have an Artifact!!!... But WTH!? is an artifact?


##  CONTINUOUS INTEGRATION

* Artifacts can be used to represent data created as a side-effect of running a build. Artifacts are files which are associated with a single build.A build can have any number of artifacts associated with it.


##  CONTINUOUS INTEGRATION

![nexus](./img/nexus.png?raw=true)
![nexus](./img/artifactory.png?raw=true)


##  CONTINUOUS INTEGRATION

* But who controls and manage all of this stuff? it's magic? DevOps people are wizards?


##  CONTINUOUS INTEGRATION

* Here is were we use a continuous integration software that supports our continuous integration process, in which developer's changes are immediately tested and reported when they are added to the mainline code base.


![ci](./img/ci.png?raw=true)


##  CONTINUOUS INTEGRATION

* Our orchestrator did the build and deploy the artifact, now what?

![jackie](./img/Jackie-chan-confused.png?raw=true) 


##  CONTINUOUS INTEGRATION

* We can't have CI without automated testing.


##  CONTINUOUS INTEGRATION

![junit](./img/JUnit_logo.png?raw=true)
![selenium](./img/selenium.png?raw=true)
![Robot](./img/robot.png?raw=true)
![bash](./img/bash.png?raw=true)


##  CONTINUOUS INTEGRATION

* But where is all this automated testing executed?


##  CONTINUOUS INTEGRATION

* Another part of CI/CD and DevOps is "Infrastructure as code", the capability of create and destroy servers under demand for specific needs or testing, with the fiability everytime will we have the same config.


##  CONTINUOUS INTEGRATION

* For local environments:

![vagrant](./img/vagrant.png?raw=true)

![compose](./img/compose.png?raw=true)


##  continuous integration

* For Public/private/Hybrid clouds: 

![terraform](./img/terraform.png?raw=true)
![cloudformation](./img/cloudformation-logo.png?raw=true)


##  continuous integration

 * How can I manage the configuration to be the same always and across all my environments?


##  continuous integration

![cm-tools](./img/cm-tools.png?raw=true)


##  CONTINUOUS INTEGRATION

How can we know the health of my environments and get alerts in time?


##  CONTINUOUS INTEGRATION

![zabbix](./img/zabbix.png?raw=true)
![graphite](./img/graphite.png?raw=true)
![prometheus_logo](./img/prometheus_logo.png?raw=true)


##  CONTINUOUS INTEGRATION

* And log management?


##  CONTINUOUS INTEGRATION

![splunk](./img/splunk.png?raw=true)
![elastic](./img/elastic.png?raw=true)
![stackdriver](./img/stackdriver.png?raw=true)

