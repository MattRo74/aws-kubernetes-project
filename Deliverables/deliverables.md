### Deliverables
1. `Dockerfile`
Link to the Dockerfile: https://github.com/MattRo74/aws-kubernetes-project/blob/master/Dockerfile

2. Screenshot of AWS CodeBuild pipeline

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/CodeBuild_Pipline_Automation.png">

3. Screenshot of AWS ECR repository for the application's repository

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/ECR_Repository.png">

4. Screenshot of `kubectl get svc`

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/KUBECTL_GET_SVC.png">

5. Screenshot of `kubectl get pods`

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/KUBECT_GET_PODS_NEW.png">

6. Screenshot of `kubectl describe svc <DATABASE_SERVICE_NAME>`

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/KUBECTL_DESCRIBE_SVC_POSTGRES-SERVICE.png">

7. Screenshot of `kubectl describe deployment <SERVICE_NAME>`

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/KUBECTL_DESCRIBE_DEPLOYMENT_COWORKING_RUNNING.png">

8. All Kubernetes config files used for deployment (ie YAML files)

Link to the YAMML Files: https://github.com/MattRo74/aws-kubernetes-project/tree/master/deployment

9. Screenshot of AWS CloudWatch logs for the application

I run out of budget and I needed to use my own AWS account. The problem is that cloudwatch is not available today:

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/CLOUDWATCH400.png">

But the application is working on AWS:

Daily Usage:
<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/CURL_DAILY_USAGE.png">

Daily Visits:

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/CURL_USER_VISITS.png">

This was the wrong (old) screenshot: 

<img src="https://github.com/MattRo74/aws-kubernetes-project/blob/master/Deliverables/CLOUDWATCH_LOG.png">


BUt I'm sure that this time the logs would be correct.

