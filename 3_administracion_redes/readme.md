# 🌍 Introducción a LocalStack

**LocalStack** es una herramienta que permite **emular servicios de AWS** en tu máquina local. Es muy útil para pruebas y desarrollo sin necesidad de una cuenta en AWS.

## 🔹 ¿Para qué se usa?

- Probar infraestructura en AWS sin costos.
- Desarrollar aplicaciones que usan AWS localmente.
- Simular servicios como **S3, Lambda, EC2, DynamoDB, API Gateway**, etc.

## 🔹 ¿Cómo funciona?

LocalStack corre en **Docker** y expone una API compatible con AWS, por lo que puedes usar **AWS CLI** o SDKs (como `boto3` en Python) para interactuar con los servicios simulados.

## 🔹 Ejemplo de Servicios Soportados

- 🚀 **EC2** → Instancias virtuales  
- 📦 **S3** → Almacenamiento de objetos  
- 🗄 **DynamoDB** → Base de datos NoSQL  
- 🏗 **CloudFormation** → Infraestructura como código  
- 🔄 **Lambda** → Funciones sin servidor  
