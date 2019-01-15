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
