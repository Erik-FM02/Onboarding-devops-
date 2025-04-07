# Ejercicio de Kubernetes: Instalación y Despliegue de una Aplicación Simple

## Objetivo
El objetivo de este ejercicio es aprender a instalar **Kubernetes** utilizando **Minikube** en una máquina local y luego desplegar una aplicación simple en un **Pod**.

---

## Paso 1: Instalar Kubernetes en tu máquina local

1. **Instalar Minikube**:
   - Investiga cómo instalar **Minikube** en tu sistema operativo. Minikube es una herramienta que permite crear un clúster de Kubernetes localmente.
   
2. **Instalar kubectl**:
   - Investiga cómo instalar **kubectl**. Esta es la herramienta de línea de comandos utilizada para interactuar con Kubernetes.

---

## Paso 2: Iniciar un clúster de Kubernetes con Minikube

1. **Iniciar Minikube**:
   - Una vez que hayas instalado Minikube, debes iniciar un clúster local. Investiga qué comando necesitas ejecutar para hacerlo.

2. **Verificar el clúster**:
   - Asegúrate de que tu clúster esté en funcionamiento. Utiliza kubectl para comprobar el estado del clúster.

---

## Paso 3: Crear y Desplegar una Aplicación Simple en Kubernetes

### 3.1: Crear un archivo YAML para un Pod

1. **Definir un Pod**:
   - Crea un archivo YAML que describa un **Pod** que ejecute una imagen de un contenedor. La imagen que debes usar es la de **nginx**, un servidor web. El contenedor debe escuchar en el puerto 80.

### 3.2: Desplegar el Pod

1. **Aplicar el archivo YAML**:
   - Utiliza `kubectl` para aplicar el archivo YAML que has creado y desplegar el Pod.

2. **Verificar el Pod**:
   - Usa `kubectl` para asegurarte de que el Pod se ha creado correctamente.

---

## Paso 4: Exponer el Pod para acceder a la aplicación

### 4.1: Crear un servicio para exponer el Pod

1. **Definir un Servicio**:
   - Crea un archivo YAML para un **Service** que exponga tu Pod en el puerto 80. El tipo de servicio debe ser **NodePort**.

### 4.2: Aplicar el archivo YAML para el servicio

1. **Aplicar el archivo YAML del servicio**:
   - Usa `kubectl` para crear el servicio que expondrá el Pod.

2. **Verificar el servicio**:
   - Comprueba que el servicio se haya creado correctamente.

### 4.3: Acceder a la aplicación

1. **Acceder al servicio**:
   - Si estás usando **Minikube**, investiga cómo acceder al servicio a través de un navegador.

---

## Paso 5: Limpiar los recursos

1. **Eliminar los recursos**:
   - Una vez que hayas probado la aplicación, elimina el Pod y el Servicio utilizando `kubectl`.

2. **Verificar que se hayan eliminado**:
   - Asegúrate de que los recursos hayan sido eliminados correctamente.

---


