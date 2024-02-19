# mlcbPlatformRepo3

This repository contains a workflow to Deploy / Undeploy to GKE CloudBees platform with **helm**.

## deploy-to-gke.yaml

This workflow contains a job called **gcloud**.

The job contains a variable called **deploy** so that when set to "true" the workflow will try to do a deployment else it will try to remove the deployment.

The job first tries to create a credential file using a secret stored in the organization. the secret must contain a valid and enabled service account token in order to successfully connect to GKE and execute helm commands.
