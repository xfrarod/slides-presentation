# What's Continuous Integration?


##  CONTINUOUS INTEGRATION

#### Continuous integration (CI) is the practice of merging all developer working copies to a shared mainline several times a day.


##  CONTINUOUS INTEGRATION

* Git

* Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

* SaaS Providers (Gitlab, Github, Bitbucket)


##  CONTINUOUS INTEGRATION

* Then... we have code and branches, now what?


##  CONTINUOUS INTEGRATION

* let's build, but... what it's a build?


##  CONTINUOUS INTEGRATION

* In the field of software development, the term build is similar to that of any other field.That is, the construction of something that has an observable and tangible result.


##  CONTINUOUS INTEGRATION

* Build automation is the process of automating the creation of a software build and the associated processes including: compiling computer source code into binary code, packaging binary code, and running automated tests.

* Tools (Maven, Gradle, Ant, Make).


##  CONTINUOUS INTEGRATION

* ok, we did a Build and now what????


##  CONTINUOUS INTEGRATION

* Now we have an Artifact!!!... But WTH!? is an artifact?


##  CONTINUOUS INTEGRATION

* Artifacts can be used to represent data created as a side-effect of running a build. Artifacts are files which are associated with a single build.A build can have any number of artifacts associated with it.

* Artifacts repositories(Artifactory, Nexus, Archiva, ...)


##  CONTINUOUS INTEGRATION

* But who controls and manage all of this stuff? it’s magic? DevOps people are wizards?


##  CONTINUOUS INTEGRATION

* Here is were we use a continuous integration software that supports our continuous integration process, in which developer's changes are immediately tested and reported when they are added to the mainline code base.

* Tools(Jenkins, TeamCity, TravisCI, ..)


##  CONTINUOUS INTEGRATION

* Our orchestrator did the build and deploy the artifact, now what?


##  CONTINUOUS INTEGRATION

* We can't have CI without automSated testing.


##  CONTINUOUS INTEGRATION

* Junit

* Selenium

* Robot

* Test with custom scripts


##  CONTINUOUS INTEGRATION

* But where is all this automated testing executed?


##  CONTINUOUS INTEGRATION

* Another part of CI/CD and DevOps is "Infrastructure as code", the capability of create and destroy servers under demand for specific needs or testing, with the fiability everytime will we have the same config.


##  CONTINUOUS INTEGRATION

* For local environments:

    * Vagrant

    * Docker Compose


##  continuous integration

* For Public/private/Hybrid clouds: 

    * Terraform

    * AWS Cloud formation. 


##  continuous integration

 * How can I manage the configuration to be the same always and across all my environments?


##  continuous integration

 * Ansible

 * Puppet 

 * Chef


##  CONTINUOUS INTEGRATION

How can we know the health of my environments and get alerts in time?


##  CONTINUOUS INTEGRATION

* Zabbix

* PagerDuty

* Graphite

* Prometheus


##  CONTINUOUS INTEGRATION

* And log management?


##  CONTINUOUS INTEGRATION

* Splunk

* Elastic Stack

* Papertrail