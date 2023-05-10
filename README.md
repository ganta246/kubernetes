# kubernetes
launch instance
give the name: kubernetes
keypair :kube-key
launch instance 
apt  install aws cli
curl -- silent  --location "https://github.com weaveworks/eksctlrelease/latest/download/eksctl_$ (uname-s)_amd64.tar.gz"! tar xz -c/tmp
sudo mv /tmp/eksctl/ /usr/local/bin
eksctl version
0.136
curl -lo https:// d1.k8s. io/release/v1.21.14/bin/linux/amd64/kubectl
sudo install -o root -g  root -m 0755 kubectl/ usr/local/bin/kubectl
kubectl version  --client
eksctl  create cluster  --name=sample-eks cluster --region=us-east-1  --version 1.22  --zones=us-east-1a,us-east1b --without-nodegroup
go to iam click 
user click and add user click
user name: k8s
provider access click
i want to create an iam user
custom passwd:
next click
attach policy select  and access aa aws managed select
next click
add perimissions
k8s click and security crendials click and
create acces key click and command line interface select and i understand select and next
description tag: sxsb
create access key click
aws configure
aws access key : 8jej021ijiodkk
aws secret key : ewtywuiwoieiuy
default region name: us-east-1
out put format : table
eksctl utils associate -iam-oidc--provider -- region us-east-1 --cluster sample-ekscluster --approve
eksctl  create  nodegroup --cluster = sample ekscluster/

-- region=us-east-1 /
--name=sample-ekscluster-ng-public1 /
--node-type=t3.small/
--nodes=2 /
--node-min =2 /
--node-max=4 /
--node-volume-size=8 /
--ssh--access /
--ssh-public-key=kube/
--managed /
--asg-access /
--external-dns-access /
--ful-ecr-access /
--appmesh-access /
alb-ingress-access /
ec2 and keypair click
keypair name:k8s
aws  eks  update-kubeconfig --region  us-east-1  --name sample-ekscluster
kubectl get nodes

pod

kubectl run my-first-pod --image stacksimplify/kubenginx:1.0.0
kubectl exec  -it my-first-pod  -- /bin/bash
kubectl get pod  my-first-pod -o yaml




