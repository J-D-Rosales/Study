Hay muchas maneras de lanzar aplicación:
- Consola web
- CLI
- IaC (CloudFormation, CDK)
- API REST
No se puede cambiar el desarrollo de producción a cada rato.
Duplicas fácilmente un entorno.
___
Crear máquina virtal con Ami.
Necesitamos el Id del Ami. En mi caso:
ami-08d434e92c0cfa0c0
___
Fargate y esas cosas.
latest: digest: sha256:9379cd9f259fbfa677c3d9af0a36cd7e6256bbce22fddfc123cbfe837c7f33c9 size: 1991
:~/books-api/Practica_aws_fargate_api_students (main) $ export IMAGE_URL=$AWS_ACCOUNT_ID.dkr.ecr.$AWS_REGION.amazonaws.com/$REPO:latest
echo $IMAGE_URL
355471816327.dkr.ecr.us-east-1.amazonaws.com/books-api:latest
}

arn de mi tonteria  AWSServiceRoleForECS|  arn:aws:iam::355471816327:role/aws-service-role/ecs.amazonaws.com/AWSServiceRoleForECS 
___
Intentádolo con api-students.
Tu **IMAGE_URL** queda así (cópialo tal cual para el despliegue):

`355471816327.dkr.ecr.us-east-1.amazonaws.com/api-students:v1`

```
STACK_NAME=api-students-fargate
VPC_ID=vpc-0c294c708c92cb54c
SUBNETS_CSV="subnet-0c6a4c9ebe841d9c1,subnet-06f36b7a6bcb65acb,subnet-06118224b4ca07f84,subnet-04ee0e9e994022d99,subnet-0a56c2b856d244959,subnet-029bc4c856b8c3748"
LAB_ROLE_ARN=arn:aws:iam::355471816327:role/LabRole
IMAGE_URL=355471816327.dkr.ecr.us-east-1.amazonaws.com/api-students:v2

aws cloudformation deploy \
  --stack-name $STACK_NAME \
  --template-file fargate-cloudformation.yml \
  --parameter-overrides \
      VpcId=$VPC_ID \
      Subnets=$SUBNETS_CSV \
      ImageUrl=$IMAGE_URL \
      LabRoleArn=$LAB_ROLE_ARN \
      ContainerPort=8000 \
      AppName=api-students \
      DesiredCount=1
```


FUENCIONONOANSDOF QOWIUAEH FOQUIEBOGIUQEBWFUQE

PRUEBITA
![[Pasted image 20250903204422.png]]
![[Pasted image 20250903204442.png]]
![[Pasted image 20250903204455.png]]
![[Pasted image 20250903204532.png]]
