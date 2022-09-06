# Description
Dummmy project to test deployment workflow into Kubernetes from a NestJS project with a monorepo structure by using ArgoCD.
Workflows are based on Github Actions, built images are stored into specific AWS ECR private repositories.

This repository simulates a typical ArgoCD repo with helm charts used to deploy into specific namespaces. Changes to this repository are pushed from github actions from repository https://github.com/CristianBB/nestJsGithubActionsMonorepo

Structure:
```
helm
|--appX
   |--templates: contains deployment, hpa, service.. 
   |--Chart.yaml
   |--values.alpha.yaml: values for alpha namespace
   |--values.beta.yaml: values for beta namespace
   |--values.production.yaml: values for production namespace
```

Githab actions just make the proper changes related to the image to be deployed into values.yaml file depending on the environment to deploy

For more info, check https://github.com/CristianBB/nestJsGithubActionsMonorepo
