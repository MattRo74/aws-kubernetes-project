### README File: documentation for your user to detail how your deployment process works and how the user can deploy changes


## 1. Create/Use a IAM User

*IAM USER:*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP00.png">


*AWS configure by creating/using access key*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP00_b.png">

## 2. Create EKS Cluster

Cluster: coworking-cluster
Node-Group: coworking-nodes

eksctl create cluster --name coworking-cluster --region us-east-1 --nodegroup-name coworking-nodes --node-type t3.small --nodes 1 --nodes-min 1 --nodes-max 2

*Update kubeconfig*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP01.png">

*show current context*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP02.png">


## 3. Configure a database for the service

*get namespaces*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP03.png">

*Configure POSTGRES Deployment*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP04.png">

*Create ENV Variables in WIN OS*

- $env:DB_PASSWORD = 'XXXXXX'
- $env:DB_USERNAME = 'coworker'
- $env:DB_HOST = '127.0.0.1'
- $env:DB_PORT = '5433'
- $env:DB_NAME = 'coworkdb'

*apply yaml-files*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP05.png">

*get pods*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP06.png">

*bash log*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP07.png">

*login to DB*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP08.png">

*list DBs*
<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP09.png">


*SEED SQLs*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP10.png">

*SELECT Tables*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP11.png">


## 4. Build the Analytics Application locally

*Install requirements in analytics folder*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP12.png">

*Forwarding DB*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP13.png">

*execute python app.py and check results*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP14.png">

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP15.png">


## 4. Build Docker Image and test it

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP16.png">

## 5. AWS

*Create ECR Repository*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP17.png">

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP18.png">


*Create CodeBuild Project*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP19.png">

*Name Project*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP20.png">

*Use Public GIT Repository*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP21.png">

*Choose Linux as EC2*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP22.png">

*Enable Privileged*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP23.png">

*Create (and change here) environment variables*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP24.png">

*Enable Cloudwatch Logs*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP25.png">

*Create CodeBuild Project*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP26.png">

*Go to IAM Roles*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP27.png">

*Add permissions*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP28.png">

*Add permissions to ECR*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP29.png">

*Save it*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP30.png">

*Login ECR*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP31.png">

*Change Variable to CODEBUILD_BUILD_NUMBER*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP32.png">

*Run CodeBuild and check Image*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP33.png">

*Check svc:*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP34.png">

*Check Couldwatch Logs*

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/images/STEP35.png">
