## Spinnaker Concepts

* Spinnaker is an open-source, multi-cloud continuos delivery platform.
* Spinnaker provides two core set of features:
    * Application Management.
    * Application Deployment.
    
## Application Management 

* Application: Management:view and manage your cloud resources.
* Objects.
    * Service Groups(SG).
    * Cluster.
    * Application.
    * Load Balancers (LB).
    * Firewalls.

## Application Management 

* Service Groups:
* Spinnaker base resource
* It identifies:
    * the deployable artifact(VM, Docker image, source location).
    * The basic configuration settings(#instances, autoscaling policies, metadata, etc.).
* This resource is optionally assosiated with LB and firewall.
* when deployed is a collection of instances of running softtware(VM instances, k8s pods).


## Application Management 

* Cluster: logical grouping of Service Group.


## Application Management 

* Application:
* Logical grouping of Clusters.
* It includes Firewalls and LB.
* It represents the service and all the configuration and infrastructure on which it will run.
* Typically you create one application per service(Spinnaker does not enforce that).


## Application Management 

* Load Balancer:
* It is associated with an ingress protocol and port range.
* Balance traffic among instances in its Server Groups.
* Optionally you can enable health checks for LB(you can define health criteria and endpoints)


## Application Management 

* Firewall:
* Defines network traffic access.
* Is a set of firewall rules defined by an IP range (CIDR) along with a protocol and port range.
* ej: 10.0.0.0/24, TCP, 8080:8080

## Application Management 

![app_management](./img/app-management.png)


## Application Deployment

* Application Deployment: Construct and manage continuos delivery workflows.
* Pipeline.
* Stage.
* Deployment strategies.

## Application Deployment

* Pipeline:
* Is the key deployment management contruct in Spinnaker.
* Like CI/CD tools it consist of a sequensce of actions, know as stages.
* can pass parameters from stage to stage along the pipeline.
* can be started manually or be triggered by an event(Jenkins job completing, Docker image appearing in you registry, a cron schedule, or stage in another pipeline)
* can send notifications by email, sms, slack to interested parties at various points during pipeline execution(such as on pipeline start/complete/fail)

![app_management](./img/pipelines.png)

## Application Deployment

* Stage:
* is an atomic building block for a pipeline.
* Describe the action that the pipeline will perform.
* The Sequence can be in any order
* Spinnaker provides a number of stages (Deploy, Resize, Disable, Manual Jugment, and many more.)

## Application Deployment

* Deployment strategies

* Spinnaker treats cloud-native deployment strategies as first class construct.
* Handle the underlying orchestration(verifying health checks, disabling old SG and enabling new ones).

## Application Deployment

* Deployment strategies:
    * Red/black (aka blue/green)
    * Rolling red/black
    * Canary

![app_management](./img/deployment-strategies.png)

## Spinnaker Architecture 

* Spinnaker is composed of independet microservices:

* Deck: Spinnaker UI.
* Gate: API Gateway.
* Orca: Pipeline Orchestrator.
* CloudDriver: make API calls to Cloud Providers Index/store deployed resources.


## Spinnaker Architecture 

* Front50: Metadata store for pipelines, apps.
* Rosco: Bakery service.
* Igor: Trigger pipelines from CI/CD Tools(Jenkins,TravisCI).
* Echo: Notification service (sms, slack, email). Also can respond to webhook(Github) 


## Spinnaker Architecture 

* Fiat: Authorization service, provides user authentication(Account, Applications, SA).
* Kayenta: platform for Automated Canary Analysis (ACA). 
* Halyard: A tool for configuring, installing, and updating Spinnaker.


# Install Spinnaker
* Spinnker requires at least 4 cores and 8GB of RAM.


# Install Spinnaker

* Spinnaker requires an external storage provider for persisting your application settings and configured pipelines.
* Data are sensitive and can be costly to lose.