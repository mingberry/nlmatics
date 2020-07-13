1.

Under this DevOps directory, there are two categories of YAML files.

The file naming convention follows as:

devops_k8s_CI_*.yaml
or)
devops_k8s_CD_*.yaml

Any file name like *_CI_*.yaml files are for Continuous Integration purpose, only can be used in the in-house development environment. Technically, they need to pull the Docker Images from the internal docker regisry, running them outside will fail. 

Any file name like *_CD_*.yaml files are for Continuous Deployment purpose, normally used on Kubernetes platform provided by a Public Cloud Provide.


2.

No matter it is a fresh install, an upgrade or just making a change, just use the same command:

$ kubectl apply -f file_name.yaml

When want to delete objects such as Pods and ReplicaSets, run the proper YMAL file(s) like this:

$ kubectl delete -f file_name.yaml


3.

The number one rule for DevOPs is: Always Use Scripts (YAML) to Make Configuration Changes.

(For Urgency, If Make a Configuration Change Manually, Document It Immediately! )  


Thanks,

Ming

