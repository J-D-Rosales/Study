
# Guía paso a paso – API Students en AWS con CDK + CloudFormation

---

## 1) Prepararaciones principales
Tenemos en cuenta que ya se ha subido la imagen el container de docker. Dónde después de abrir los puertos necesarios, y correr el contenedor, ha comprobado que funcione. 

- App Flask en `app.py`, expone `/students` en `0.0.0.0:8000`.
- Dockerfile para empaquetar la app.
- Imagen ya subida a ECR:
    ```
    355471816327.dkr.ecr.us-east-1.amazonaws.com/api-students:v2
    ```
Cabe recalcar que es un paso sumamente importante cambiar los grupos de seguridad, para no tener bloqueos.
Tener tu imagen subida a amazon.
Asimismo se debe tener condigurado los aws credentials. El cual cómo estamos usando AWS Learner lab, están en aws details.

## 2) Configurar proyecto CDK

Creamos un directorio con el nombre de api-students-cdk.

```
api-students-cdk/
├─ bin/api-students.ts
├─ lib/api-students-stack.ts
├─ cdk.json
├─ package.json
└─ tsconfig.json
```

Y debemos tener todos estos archivos. (No confundirse con ejecutar comandos dentro de bin/ o de lib/) Los comandos se ejecutan en la raiz principal)
Usamos **BootstraplessSynthesizer** → no depende de bootstrap (necesario en AWS Learner Lab).
EL cdk es:
```
{
  "app": "npx ts-node --prefer-ts-exts bin/api-students.ts",
  "context": {
    "imageUri": "355471816327.dkr.ecr.us-east-1.amazonaws.com/api-students:v2",
    "containerPort": 8000,
    "labRoleArn": "arn:aws:iam::355471816327:role/LabRole",
    "desiredCount": 1,
    "cpu": 256,
    "memoryMiB": 512,
    "region": "us-east-1",
    "useDefaultVpc": true
  }
}
```

---
## 3) Instalar dependencias

```bash
cd ~/contenedores/api-students-cdk
npm install
```
Debemos aclarar por experiencia propia que se debe instalar en la raiz del proyecto. 

---

## 4) Generar plantilla CloudFormation (YAML)

```bash
npx cdk synth \
  -c imageUri=355471816327.dkr.ecr.us-east-1.amazonaws.com/api-students:v2 \
  -c containerPort=8000 \
  -c labRoleArn=arn:aws:iam::355471816327:role/LabRole \
  -c desiredCount=1 \
  > cdk-out.yml
```

El archivo `cdk-out.yml` es la plantilla lista para desplegar.
![[Screenshot from 2025-09-08 10-48-51.png]]

---
Usamos el siguiente comando para deployar- esto puede tardar ciertos momentos, pero debería salirte create in progress.
```bash
aws cloudformation deploy \
  --stack-name api-students-cdk \
  --template-file cdk-out.yml \
  --capabilities CAPABILITY_IAM CAPABILITY_NAMED_IAM
```

Esto creará
- **VPC**
- **ECS Cluster**
- **Fargate Service**
- **Application Load Balancer**
![[Screenshot from 2025-09-08 10-51-20.png]]
Podemos ir checkeando el progreso en CloudFormation.
![[Screenshot from 2025-09-08 10-52-59.png]]
Una vez completado, deberá salir create complete. Con eso podrás sacar el DNS.
## 6) Obtener DNS del Load Balancer

```bash
DNS=$(aws cloudformation describe-stacks \
  --stack-name api-students-cdk \
  --query "Stacks[0].Outputs[?OutputKey=='LoadBalancerDNS'].OutputValue" \
  --output text)

echo "ALB DNS: $DNS"
```
![[Screenshot from 2025-09-08 10-56-40.png]]
---
Probamos la consola con postma (se deja de evidencia las capturas)

![[Pasted image 20250908105712.png]]
![[Pasted image 20250908105731.png]]
![[Pasted image 20250908105739.png]]
![[Pasted image 20250908105747.png]]
![[Pasted image 20250908105754.png]]
___
## 9) Eliminar recursos (cleanup)

Para no dejar nada corriendo:

```bash
aws cloudformation delete-stack --stack-name api-students-cdk

aws cloudformation wait stack-delete-complete --stack-name api-students-cdk
```

Verifica que ya no exista:

```bash
aws cloudformation describe-stacks --stack-name api-students-cdk
# debería dar error "does not exist"
```

---
