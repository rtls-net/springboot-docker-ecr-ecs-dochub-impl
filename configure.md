**--install  AWS in window machine**
download AWSCLIV2 in your machine and proceed with normal software install
 
**--configure aws account in aws cli**
cmd>aws configure

provide genarated IAM acces key and secreat key

**-- push image to ECR registry**
cmd> aws ecr get-login-password | docker login --username AWS --password-stdin <ECR main url without registry name>

**--Build Docker image**
maven build then you need to tag docker image like 
docker tag <image>:<tag> <ECR Full registry with repo name>

**--Docker push**
docker push <ECR Full registry with repo name>






**-- BUild Docker Image**
docker build -t <Image> .
