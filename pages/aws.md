# AWS

![Untitled](/imgs/aws.png)

## Introdução
- [AWS In 5 Minutes | What Is AWS? | AWS Tutorial For Beginners | AWS Training | Simplilearn (youtube.com)](https://www.youtube.com/watch?v=3XFODda6YXo&ab_channel=Simplilearn)

- [Indtrodução a AWS](https://www.youtube.com/watch?v=Z3SYDTMP3ME&list=PLzk4R2ZiwXBEkRApbKf1SG7N_H-sMmQ2o&index=5&ab_channel=AWSwithChetan)

- [AWS Fundamentals: Beginners Guide
](https://medium.com/age-of-awareness/aws-fundamentals-beginners-guide-ffea402596fb)



## Fundamentos

### AWS CLI

O CLI é uma sigla para  `Comand Line Interface` ou Interface de linha de comando. Por meio desse pacote é possível que enviamos comandos diretos para a AWS por meio de instrução codificadas no terminal do sistema operacional.

```bash
aws s3 ls
```

### AWS SDK para Python

O `boto3` é um SDK, Toolkit ou um conjunto de código para Python. Esse conjunto é denominado de biblioteca. Com ela podemos fazer interações com os serviços da AWS por meio de API's e funções disponível.

```python
import boto3
# Cria um recurso do S3
s3 = boto3.resource("s3")
# Cria um bucket do S3 com o nome "meu-bucket-boto3"
bucket = s3.create_bucket(Bucket="meu-bucket-boto3")
# Faz upload de um arquivo local chamado "meu-arquivo.txt" para o bucket
bucket.upload_file("meu-arquivo.txt", "meu-arquivo.txt")
# Lista todos os buckets do S3 em sua conta
for bucket in s3.buckets.all():
print(bucket.name)
```

## Serviços Gerais

```
💡 [Introduction to AWS Services - YouTube](https://www.youtube.com/watch?v=Z3SYDTMP3ME&list=FLc8jEdxLESWM-uIGCggc0Xw&index=10&t=1786s&ab_channel=AWSwithChetan)
Esse vídeo monstra um desesenho de arquitetura simples de uma empresa utiilizando serviços onpremisse vs o serviço correspondente na AWS
```

Os serviços abaixo da AWS são usados para diferentes propósitos e podem ser classificados em diferentes categorias. Algumas diferenças entre eles são:

### VPC

[AWS VPC Introduction. What is AWS VPC? | by MrDevSecOps | Medium](https://medium.com/@mrdevsecops/aws-vpc-introduction-b62fa9f6a456)

![Untitled](/imgs/aws_vpc.png)

VPC é a sigla para Virtual Private Cloud, que é um serviço que permite criar uma rede virtual isolada na nuvem da AWS. Com o VPC, é possível definir o seu próprio espaço de endereçamento IP, sub-redes, tabelas de rotas, gateways e regras de segurança. O VPC é um serviço da categoria de rede e entrega de conteúdo.

### IAM

![Untitled](/imgs/aws_iam.png)

IAM é a sigla para Identity and Access Management, que é um serviço que permite gerenciar o acesso aos recursos da AWS. Com o IAM, é possível criar usuários, grupos, papéis e políticas de permissão. O IAM é um serviço da categoria de segurança, identidade e conformidade.

### IAM polices for Lambda

![Untitled](/imgs/aws_iam_polices.png)

IAM polices for Lambda são políticas de permissão do IAM que permitem controlar o acesso das funções do Lambda aos recursos da AWS. Com essas políticas, é possível definir quais ações o Lambda pode executar e em quais recursos. As políticas do IAM são um recurso do serviço IAM, enquanto o Lambda é um serviço da categoria de computação.

### ACL - AWS Access Control List

ACL é a sigla para Access Control List, que é um recurso que permite controlar o acesso aos seus buckets e objetos do S3. Com o ACL, é possível definir quais usuários ou grupos podem ler ou escrever nos seus dados armazenados no S3. O ACL é um recurso do serviço S3, que é um serviço da categoria de armazenamento.

### CloudFormation

![Untitled](/imgs/aws_cloudformation.png)

CloudFormation é um serviço que permite criar e gerenciar recursos da AWS usando modelos declarativos. Com o CloudFormation, é possível descrever a infraestrutura desejada em um arquivo JSON ou YAML e aplicá-lo na nuvem da AWS. O CloudFormation é um serviço da categoria de gerenciamento e governança.

### CodeBuild

![Untitled](/imgs/aws_codebuild.png)

CodeBuild é um serviço que permite compilar, testar e empacotar o seu código-fonte na nuvem da AWS. Com o CodeBuild, é possível integrar o seu código com outros serviços da AWS, como o CodeCommit, o CodeDeploy e o CodePipeline. O CodeBuild é um serviço da categoria de ferramentas para desenvolvedores.

### Step Function

![Untitled](/imgs/aws_sfn.png)

Step Function é um serviço que permite coordenar componentes distribuídos e sem estado em fluxos de trabalho escaláveis. Com o Step Function, é possível criar aplicações complexas usando funções do Lambda, atividades do ECS, tarefas do Batch e outros serviços da AWS. O Step Function é um serviço da categoria de aplicação.

### Route 53

![Untitled](/imgs/aws_route53.png)

Route 53 é um serviço que oferece um sistema de nomes de domínio (DNS) na nuvem da AWS. Com o Route 53, é possível registrar domínios, gerenciar zonas hospedadas, rotear tráfego e monitorar a saúde dos seus endpoints. O Route 53 é um serviço da categoria de rede e entrega de conteúdo.

### EBS

![Untitled](/imgs/aws_ebs.png)

EBS é a sigla para Elastic Block Store, que é um serviço que oferece volumes de armazenamento em bloco persistentes para as suas instâncias do EC2. Com o EBS, é possível escolher entre diferentes tipos e tamanhos de volumes, além de tirar snapshots e criar backups dos seus dados. O EBS é um serviço da categoria de armazenamento.

### S3 LifeCycle

![Untitled](/imgs/aws_s3_lifecicle.png)

S3 LifeCycle é um recurso que permite gerenciar o ciclo de vida dos seus objetos do S3. Com o S3 LifeCycle, é possível definir regras para mover os seus dados entre as classes de armazenamento do S3, como o S3 Standard, o S3 Infrequent Access e o S3 Glacier. O S3 LifeCycle é um recurso do serviço S3, que é um serviço da categoria de armazenamento.

### Cloudwatch

[Como o Amazon CloudWatch funciona - Amazon CloudWatch](https://docs.aws.amazon.com/pt_br/AmazonCloudWatch/latest/monitoring/cloudwatch_architecture.html)

![Untitled](/imgs/aws_cloudwatch.png)

Cloudwatch é um serviço que permite monitorar e observar os seus recursos e aplicações na nuvem da AWS. Com o Cloudwatch, é possível coletar métricas, logs, eventos e alarmes dos seus serviços da AWS e visualizá-los em painéis ou gráficos. O Cloudwatch é um serviço da categoria de gerenciamento e governança.

![Untitled](/imgs/aws_cloudwatch_2.png)

### SNS

[Amazon SQS vs Amazon SNS. Amazon SQS and Amazon SNS are the two… | by Aram Koukia | Koukia](https://koukia.ca/amazon-sqs-vs-amazon-sns-2609d15b213b)

![Untitled](/imgs/aws_sns.png)

SNS é a sigla para Simple Notification Service, que é um serviço que permite enviar notificações para diferentes destinos, como email, SMS ou HTTP endpoints. Com o SNS, é possível publicar mensagens em tópicos e assinar os seus consumidores para receber as notificações. O SNS é um serviço da categoria de aplicação.

![Untitled](/imgs/aws_sns_2.png)

### Glue

[AWS Cloud Data Engineering End-to-End Project — AWS Glue ETL Job, S3, Apache Spark | by Dogukan Ulu | Medium](https://medium.com/@dogukannulu/aws-cloud-data-engineering-end-to-end-project-aws-glue-etl-job-s3-apache-spark-967d6ebe1d88)

![Untitled](/imgs/aws_glue.png)

Glue é um serviço que permite extrair, transformar e carregar (ETL) dados na nuvem da AWS. Com o Glue, é possível descobrir, catalogar e preparar os seus dados para análise usando crawlers, catálogos e jobs. O Glue é um serviço da categoria de análise.

## Data Tools

Os Data Tools são ferramentas da AWS que permitem criar, gerenciar e acessar fontes de dados na nuvem. Algumas dessas ferramentas são:

- **Job Bookmarks:** um recurso do AWS Glue que permite rastrear o progresso dos jobs de ETL (extração, transformação e carga) e garantir a consistência dos dados processados. Os job bookmarks podem ser usados para lidar com dados incrementais, evitando a duplicação ou a perda de registros.
- **Crawler:** um serviço do AWS Glue que explora as fontes de dados e cria metadados sobre elas, armazenando-os no AWS Glue Data Catalog. O crawler pode detectar o esquema, o formato, a partição e a classificação dos dados, facilitando o acesso e a análise posterior.
- **EMR:** um serviço da AWS que permite executar clusters de big data na nuvem, usando frameworks como Apache Spark, Apache Hadoop, Apache Hive e outros. O EMR oferece escalabilidade, flexibilidade e segurança para processar grandes volumes de dados de forma rápida e econômica.
    - **AWS S3DistCp (s3-dist-cp):** um utilitário do EMR que permite copiar grandes quantidades de dados entre o Amazon S3 e o HDFS (Hadoop Distributed File System), ou entre dois buckets do S3. O s3-dist-cp usa múltiplas threads para acelerar a transferência e pode lidar com arquivos comprimidos ou particionados.

## Athena

[https://sol.sbc.org.br/livros/index.php/sbc/catalog/download/80/346/605-1?inline=1](https://sol.sbc.org.br/livros/index.php/sbc/catalog/download/80/346/605-1?inline=1#:~:text=O%20conjunto%20de%20dados%20resilientes,do%20RDD%20em%20diferentes%20parti%C3%A7%C3%B5es.)

![Untitled](/imgs/aws_athena.png)

O Athena é um serviço da AWS que permite executar consultas SQL sobre dados armazenados no Amazon S3, sem a necessidade de configurar ou gerenciar servidores. É um serviço serverless, que cobra apenas pelo volume de dados processados. Nele é possível acessar os metadados criados pelo AWS Glue Crawler, além de ter suporte vários formatos de dados, como CSV, JSON, ORC, Parquet e Avro.

> *As Amazon Athena is serverless, which makes it quicker and easier to execute the queries on Amazon S3 without taking care of the server and the cluster to set up or manage. Another thing is the initialization time, in Athena, we can straight away query the data on Amazon S3, but in Redshift, we have to wait for the cluster to get active and once the cluster is activated, only then we are allowed to query the data.*
>
- **MSCK REPAIR TABLE**

    O `MSCK REPAIR TABLE` é um comando `SQL` do `Athena` que permite sincronizar os metadados do `AWS Glue Data Catalog` com os dados reais no `Amazon S3`. Esse comando é útil quando há alterações nos dados ou nas partições que não foram detectadas pelo `crawler`.


## AWS Redshift

![Untitled](/imgs/aws_redshift.png)

O `Redshift` é um serviço que oferece um data warehouse na nuvem, otimizado para análises complexas sobre grandes conjuntos de dados estruturados ou semi-estruturados. O Redshift usa uma arquitetura de colunas, que melhora o desempenho das consultas, e uma tecnologia de compressão, que reduz o espaço de armazenamento. Também possui integração com outros serviços da AWS, como o `S3`, o `EMR`, o `Athena` e o `Sagemaker`.

- **AWS Redshift Spectrum**

    ![Untitled](/imgs/aws_redshift_spectrum.png)

    O Spectrum é um recurso do Redshift que permite executar consultas SQL sobre dados armazenados no Amazon S3, sem a necessidade de carregá-los para o Redshif. O Spectrum também pode acessar os metadados do AWS Glue Data Catalog, alem de suportar vários formatos de dados, como CSV, JSON, ORC, Parquet e Avro.

    <aside>
    💡 Com o Spectrum é possível combinar dados que estão armazenados S3 com dados do Redshift em uma única consulta.

    </aside>


## AWS Sagemaker

![Untitled](/imgs/aws_sagemaker.png)

O Sagemaker é um serviço da AWS que permite criar, treinar e implantar modelos de machine learning na nuvem. Esse serviço oferece um ambiente integrado e interativo para :

- Explorar os dados
- Construir os algoritmos
- Usar notebooks Jupyter e bibliotecas populares como TensorFlow, PyTorch e MXNet.

O Sagemaker também oferece recursos para otimizar o treinamento, como distribuição automática, ajuste automático e detecção automática de erros. Além disso, o Sagemaker facilita a implantação dos modelos em produção, com escalabilidade, segurança e monitoramento.

## AWS DMS

O DMS (Database Migration Service) é um serviço da AWS que permite migrar dados de bancos de dados relacionais ou não relacionais para a nuvem, ou entre diferentes plataformas na nuvem. Capaz de suportar diversos tipos de bancos de dados:

1. Oracle
2. MySQL
3. PostgreSQL
4. MongoDB
5. DynamoDB e outros.

O DMS pode realizar migrações completas ou incrementais, preservando a integridade e a consistência dos dados.

## AWS Cost Explorer

O Cost Explorer é uma ferramenta da AWS que permite visualizar e analisar os custos e o uso dos serviços da AWS. Além disso, oferece gráficos interativos e relatórios personalizados, que podem ajudar a identificar tendências, padrões e oportunidades de otimização. Ele também permite criar orçamentos e alertas, para controlar os gastos e evitar surpresas na fatura.