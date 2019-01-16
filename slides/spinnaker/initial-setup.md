## initial setup

* Make sure you have properly configured gcloud [gcloud-config](../gcp-sdk-cli-essentials/config.md)

* More Documentation about Org settup can be find in [managing-gcp-with terraform](https://cloud.google.com/community/tutorials/managing-gcp-projects-with-terraform)

```bash
#Scrit to create required service account for Terraform
wget https://gist.githubusercontent.com/gmlp/63f5811f2ec8a8772e47ba8ee5c5960f/raw/4af7e97a444d68b2a850576d727e02163a74460b/gke-terraform-initial-setup.sh 

chmod +x gke-terraform-initial-setup.sh

./gke-terraform-inital-setup.sh

```