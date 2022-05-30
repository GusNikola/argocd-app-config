#About project

I'm doing this project to learn how to use one cool tool, called ArgoCD.

The assumption is that we have a separate repository for the source code, and a repository for the configuration files of the kubernetes cluster on which our application will run. There should also be a CD script inside the repository in which the source code is located, which would create a Docker image of the application, and push it on the Docker Hub.



##Workflow
After the developers develop a new version of the application, they should write a new version of the deployment file, which this time will make PODs from the docker image of the new version of the application, and they will have to push the new version of the deployment file to the configuration file repository. The ArgoCD will then detect the change in the configuration file repository and apply the changed file to the cluster to which it is linked.

##My setup
- Linux operating system (ubuntu distribution)
- Minikube , to quickly set up a local Kubernetes cluster
- Since I don't have a separate source code repository from which to make docker images and upload them to the docker hub, I will use the docker images from this link
https://hub.docker.com/r/nanajanashia/argocd-app/tags
- I will use feature branching strategy, each branch will be named after the id of task that is solved on that branch

##Tasks
1.: Write deployment and service yaml files for the application, version 1.0 of the application
2.: Write the Application.yaml file to use when configuring ArgoCD
3.: Update kubernetes configuration files to test sync

