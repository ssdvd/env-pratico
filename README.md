# Um app "hello world" nodejs com um cluster de alta disponibilidade e escalabilidade. 

Utilizando IaC:

Terraform.

Build de imagem:

Docker.

Cloud AWS, foi utilizados os serviços:

S3 - Para armazenar o estado do Terraform;

Load Balancer - Para balanceamento das requisições;

ASG - Para escalabilidade;

ECS, EKS, FARGATE - o app;

ECR - Armazenamento de imagem buildada através do docker

CloudWatch - Monitoramento.
