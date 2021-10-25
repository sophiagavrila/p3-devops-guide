# Operation: Deploy to AWS EKS
In order to connect to the kubernetes cluster managed by AWS, you will need download the AWS CLI.  For Windows, go [here](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-windows.html); Mac  users go [here](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-mac.html).

1. Once you have the AWS CLI installed, open up Commpand Prompt/terminal and run the following to confirm:

```
$ aws --version
aws-cli/2.1.29 Python/3.7.4 Linux/4.14.133-113.105.amzn2.x86_64 botocore/2.0.0
```

<br>

2. To connect to the cluster & use `kubectl` commands through the AWS CLI, you'll need to run the following commands:

```
aws configure --profile personal 

1. <access key> 
2. <secret access key> 
3. us-east-1 
4. json 

aws eks --profile personal update-kubeconfig --name Sophia-P3-Cluster --region us-east-1
```

<br>

*Now you're connected to the cluster!*

<br>

4. You can run ``

## `kubectl` commands

<br>

|     Kubernetes Command       |     Description          |
| ------------- | ------------- |
| kubectl apply -f filename | To create a deployment/service/configmap based on a given YAML file |
| kubectl get all | To get all the components inside your cluster |
| kubectl get pods | To get all the pods details inside your cluster |
| kubectl get pod pod-id | To get the details of a given pod id |
| kubectl describe pod pod-id | To get more details of a given pod id |
| kubectl delete pod pod-id | To delete a given pod from cluster |
| kubectl get services | To get all the services details inside your cluster |
| kubectl get service service-id | To get the details of a given service id |
| kubectl describe service service-id | To get more details of a given service id |
| kubectl get nodes | To get all the node details inside your cluster |
| kubectl get node node-id | To get the details of a given node |
| kubectl get replicasets | To get all the replica sets details inside your cluster |
| kubectl get replicaset replicaset-id | To get the details of a given replicaset |
| kubectl get deployments | To get all the deployments details inside your cluster |
| kubectl get deployment deployment-id | To get the details of a given deployment |
| kubectl get configmaps | To get all the configmap details inside your cluster |
| kubectl get configmap configmap-id | To get the details of a given configmap |
| kubectl get events --sort-by=.metadata.creationTimestamp | To get all the events occured inside your cluster |
| kubectl scale deployment accounts-deployment --replicas=3 | To increase the number of replicas for a deployment inside your cluster |
| kubectl set image deployment accounts-deployment accounts=eazybytes/accounts:k8s | To set a new image for a deployment inside your cluster |
| kubectl rollout history deployment accounts-deployment | To know the rollout history for a deployment inside your cluster |
| kubectl rollout undo deployment accounts-deployment --to-revision=1 | To rollback to a given revision for a deployment inside your cluster |
| kubectl autoscale deployment accounts-deployment --min=3 --max=10 --cpu-percent=70 | To create automatic scaling using HPA for a deployment inside your cluster |
| kubectl logs node-id | To get a logs of a given node inside your cluster |


https://www.eksworkshop.com/beginner/050_deploy/
