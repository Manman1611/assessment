Task1: 
    a> Created a Dockerfile for a simple golang webserver 
    b> Build Docker image using Dockerfile
    c> Push the images to image registry(Dockerhub,AWS ECR)

    Commands to be used

    -> Creating ECR Registry and login in to ecr.
        aws ecr create-repository --repository-name hello-world --image-scanning-configuration scanOnPush=true --region us-east-1
        aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin aws_account_id.dkr.ecr.region.amazonaws.com

    -> Build Container Image & pushing in to ECR.

        docker build -t <aws_account_id>.dkr.ecr.us-east-1.amazonaws.com/imagename:<tag> .
        docker push <aws_account_id>.dkr.ecr.us-east-1.amazonaws.com/imagename:<tag>
    

Task2:
    Create Minikube Cluster

        a> Apply manifest files on minikube cluster.
            kubectl apply -f filename.yml -n namespace

Task3:
    a> Creation of terraform files.
    b> Commands to be used -->
        1> terraform init
        2> terraform plan 
        3> terraform apply

    1> providers.tf
    2> k8s.tf

Task4:

    Created a automation.sh script which will automate the above task.
# Searchlabs-Assesment
