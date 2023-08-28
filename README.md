# K8s-
cluster setup for sas viya 4 

# Cluster Setup
SAS Viya deployment requires experience with Kubernetes. However, SAS provides tools to help administrators create and configure a cluster that meets SAS Viya system requirements.
The SAS Viya Infrastructure as Code (IaC) projects contain scripts and configuration files that can automatically provision the infrastructure components that are required to deploy SAS Viya on AWS.
https://github.com/sassoftware/viya4-iac-aws
# Required Permissions
Deploying the software and running tasks to operate SAS Viya servers require administrative access to the cluster and to the one or more namespaces that are used. For example, any user who issues kubectl commands to operate or check the status of SAS Viya servers will need this level of access. In the SAS Viya documentation, this level of access is referred to as elevated Kubernetes permissions.

# Create a Role named "pod-reader" that allows users to perform get, watch and list on pods:
 kubectl create role pod-reader --verb=get --verb=list --verb=watch --resource=pods
