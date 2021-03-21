# Samples for ArgoCD

This repository contain code and configuration files that could be used for an ArgoCD demonstration or for educations.

* app. It contains the code of the application used the sample. The application is a basic one written in GoLang.
* app_config. It contains the basic files defining that could be used for application deployment. It uses the Kustomise feature to identify all the yaml file. 
* app_dev. It containt the deployment file used to deploy the sample in dev environment. In this case, a namespace named `test-app-dev`. The `application.yaml` file defines the application in ArgoCD. The `kustomization.yaml` adjust the deployment files for the specific dev environment (route customisation, namespace).
* app_prod. It containt the deployment file used to deploy the sample in prod environment. In this case, a namespace named `test-app-prod`. The `application.yaml` file defines the application in ArgoCD. The `kustomization.yaml` adjust the deployment files for the specific prod environment (route customisation, updated value in configmap, namespace).
* argocd. It contains the files to deploy the ArgoCd instance.
* docs. It is a directory wi `.md` files explaining the samples of this repository. 
* MQ. It constain the deployment of a MQ instance on CP4I managed by ArgoCD. 

This repository contains 3 samples
1. The [deployment of ArgoCD instance](./docs/deploy_argocd.md) on OpenShift. 
2. The [deployment of an application](./docs/app_deployment.md) in dev and prod environments. Each environment has its own specificities (routes, namespace, config values ...).
3. The [deployment of a MQ instance](./docs/mq_deployment.md) managed by ArgoCD. 
