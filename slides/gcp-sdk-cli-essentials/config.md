## configure cli 

``` bash
# Authenticate
gcloud auth login 

# set a default project
gcloud config set project $(gcloud projects list | tail -1 | awk '{print $1}')
```