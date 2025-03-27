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


# Administración de Redes con LocalStack

En esta categoría aprenderás a simular redes y servicios de AWS en local utilizando LocalStack. Trabajaremos con VPCs, subredes y buckets S3 para backups.

---

## **Ejercicios**

1. **VPC y red básica**  
   Configura una red virtual simulada con una tabla de enrutamiento y un gateway de Internet.

2. **Subredes en la VPC**  
   Crea subredes públicas y privadas en la VPC simulada y asócialas a instancias.

3. **S3 para backups**  
   Configura un bucket S3 para almacenar datos simulados con políticas de acceso personalizadas.

---

## **Requisitos previos**

- Instalar [LocalStack](https://github.com/localstack/localstack).
- Configurar el AWS CLI para apuntar a LocalStack.
