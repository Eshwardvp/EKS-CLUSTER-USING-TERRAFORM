Clone into local or EC2 Instance

Execute these commands

terraform init

terraform apply
terraform approve --auto-approve

## Install AWS CLI client in your machine

curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install


## Configure your aws account with accesskey & secret key

aws configure

Get the accesskey & secret key from aws account and execute aws configure

## Install Terraform on ubuntu if you dont have it in your or vm or local

## UBUNTU

wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install terraform

## WINDOWS

https://releases.hashicorp.com/terraform/1.8.0/terraform_1.8.0_windows_amd64.zip



### Install kubectl

curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.24.17/2024-01-04/bin/linux/amd64/kubectl

sha256sum -c kubectl.sha256

chmod +x ./kubectl

mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$HOME/bin:$PATH

kubectl version --client

## provide your region code & clustername

aws eks update-kubeconfig --region region-code --name my-cluster

(eg: aws eks update-kubeconfig --region ap-southeast-1 --name poc-eks)


Install Grafana & Prometheus in the machine

