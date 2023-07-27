
# micro-demo
# In this project, I deployed a microservice application, packaged it with Helm and deployed it to a Kubernetes Cluster via a CI/CD pipeline and the project can be access via the Cluster IP. The beauty of Helm is that it packages the deployment into a single file. Thereby it acts as a package manager for Kubernetes apps. 
# Instead of working on mulltiple YAML deployment files, you just install the Helm Chart using a single command "Helm install <name>"
# Prerequisites:  Azure Subscription, Kubernetes Cluster, Container Registry, Azure DevOps for CI/CD pipeline.
# I used the Azure portal to deploy two resources, a Kubernetes Cluster (AKS) and container registry. 
# Then I pushed my micro-service app to Github.
# I created a continuous integration pipeline using Azure Devops to pull the code from my Github repository, build it using helm and push the artifact into the container registry.
# Then I created a release continous deployment pipeline to pull the already packaged artifact from the container registry and deploy into the Kubernetes Cluster.
# Finally I was able to access the deployed app using the load balancer IP on my local machine. See screenshots attached.


![create release](https://github.com/Lofty900/micro-demo/assets/78558689/3abbacd6-15ff-4107-add0-4e7ef9cd58fd)
![create release](https://github.com/Lofty900/micro-demo/assets/78558689/8dfd09c0-acf0-4e3c-8ddf-273a1f8f03ff)
![release created](https://github.com/Lofty900/micro-demo/assets/78558689/ea9a1295-6f6a-4cc0-8149-9c8358bf2c88)
![helm chart successfully deployed](https://github.com/Lofty900/micro-demo/assets/78558689/48d0948b-883f-4f6b-915c-e14e36d3c7a0)

![release successful](https://github.com/Lofty900/micro-demo/assets/78558689/e3ba9bc5-2816-46ef-ac46-fdc00a523566)
![pipeline](https://github.com/Lofty900/micro-demo/assets/78558689/3485e388-f512-4d7a-a1ea-88922d895bdb)
![deploy](https://github.com/Lofty900/micro-demo/assets/78558689/c5090f0d-8a7f-41f7-bdc9-0967b640e36a)
![succeeded](https://github.com/Lofty900/micro-demo/assets/78558689/48e480a1-2f47-4b02-90f5-c2c9fa71df3c)
