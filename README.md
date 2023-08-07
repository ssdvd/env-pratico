# App "Hello World" Node.js com Cluster de Alta Disponibilidade e Escalabilidade

Este projeto é um exemplo de um aplicativo "Hello World" Node.js que demonstra a configuração de um cluster de alta disponibilidade e escalabilidade utilizando Infrastructure as Code (IaC) com Terraform e tecnologias relacionadas na nuvem AWS (Amazon Web Services).

## Tecnologias Utilizadas

- **Terraform**: Utilizado para provisionar a infraestrutura como código.
- **Docker**: Utilizado para construir e empacotar a imagem do aplicativo.
- **AWS (Amazon Web Services)**: A nuvem utilizada para hospedar o cluster e os serviços relacionados.
  - **S3**: Armazenamento do estado do Terraform.
  - **Load Balancer**: Balanceamento das requisições entre instâncias.
  - **ASG (Auto Scaling Group)**: Escalabilidade automática do cluster.
  - **VPC (Virtual Private Cloud)**: Configuração de múltiplas Availability Zones (AZs) para alta disponibilidade.
  - **ECS, EKS, Fargate**: Plataformas de orquestração de contêineres para executar o aplicativo.
  - **ECR (Elastic Container Registry)**: Armazenamento de imagens de contêineres construídas com Docker.
  - **CloudWatch**: Monitoramento e Health Checks.

## Pré-requisitos

- [Terraform](https://www.terraform.io/downloads.html) instalado localmente.
- Conta na AWS com credenciais configuradas.
- Docker instalado para construir a imagem do aplicativo.

## Como Usar

**Clone este repositório:**

git clone https://github.com/ssdvd/terraform-cluster-docker-nodejs

cd terraform-cluster-docker-nodejs

**Crie uma instância do terraform.tfvars e defina suas variáveis de ambiente:**

cp terraform.tfvars.example terraform.tfvars

**Inicialize o Terraform:**

terraform init

**Edite o arquivo terraform.tfvars e insira suas configurações**

**Construa a imagem Docker do aplicativo:**

docker build -t hello-world-app ./docker-node

**Execute o aplicativo em um ambiente de contêiner para validar:**

docker run -p 8080:8080 hello-world-app

Acesse o aplicativo no seu navegador em http://localhost:8080.

Em seguida suba a imagem para o repositório EKS na AWS.

**Aplique o Terraform:**

terraform apply


## Notas
Este é um projeto de exemplo e não é adequado para ambientes de produção sem ajustes adicionais.
Certifique-se de revisar e entender a infraestrutura que será provisionada antes de executar o Terraform.
