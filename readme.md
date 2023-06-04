
O LocalStack fornece uma estrutura de teste/simulação fácil de usar para o desenvolvimento de aplicativos em nuvem. Isso significa que você pode testar os recursos da nuvem AWS localmente em sua máquina.
Nota: LocalStack compatível apenas com pilha de nuvem AWS .

O LocalStack ativa as seguintes APIs principais da nuvem em sua máquina local.

1. ACM, API Gateway, CloudFormation, CloudWatch
2. CloudWatch Logs, DynamoDB, DynamoDB Streams
3. EC2, Elasticsearch Service, EventBridge (CloudWatch Events)
4. Firehose, IAM, Kinesis, KMS, Lambda, Redshift
5. Route53, S3, SecretsManager, SES, SNS
6. SQS, SSM, StepFunctions, STS

### Benefícios
1. Reduzir o custo
2. Teste o recurso da nuvem AWS localmente
3. Depurar localmente


### Como executar:
```
sudo docker-compose up
```

### Testar
http://localhost:4566/health

### Criando uma fila SQS
```
aws --endpoint-url=http://localhost:4566 sqs create-queue --queue-name queueName
```

Mais infos: https://onexlab-io.medium.com/localstack-sqs-a0c36fd13108