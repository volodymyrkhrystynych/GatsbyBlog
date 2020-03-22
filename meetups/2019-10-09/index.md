# Containers and Hybrid Cloud
## WeCloudData

Containers started with FreeBSD coming out with a jail command for the os to isolate a process
2013 - Docker was released as an open-source project

Containers are isolated and are shipped with everything that they need to run, so that the container does not need to be run on an OS 

Basic container Components
 1. Container engine
 2. Base container image
 3. Image/container repository/registry
 4. Container network
 5. Services
 6. Build file

## Benefits
 - Containers are extremely portable
 - Reduce OS licensing
 - Reduce security risk by removing the OS as an attack vector
 - Increase in application performance
 - Containers work really well with the cloud
 - Eliminate vendor lockin

What is hybrid cloud? Cloud on a case by case basis.

Orchestration with Kubernetes or swarm

You can have a Kubernetes federation where you have Kubernetes on aws, azure and other cloud services all talking to one another and maintaining the same policies everywhere and reduces overhead

Containers are a neutral format unlike virtual machines, it is much harder to bail on AWS with virtual machines because the virtual machine are different between each cloud provider

Containers might not be suited to gpu ml, however if it is on the cloud then all that is is api calls

It is best when the makers of an application, if microsoft has containerized word then you can use it as a dependency, but other wise you might be out of luck










