# ** Proyecto: Análisis de Red y Seguridad con Nmap**

## **Objetivo:**
El objetivo de este mini proyecto es que adquieran experiencia práctica utilizando **Nmap**, una de las herramientas más poderosas para el descubrimiento de redes, auditoría de seguridad y mapeo de puertos. A lo largo de este proyecto, realizarás escaneos de red para identificar puertos abiertos, servicios, sistemas operativos y posibles vulnerabilidades, mientras aplicas conceptos de seguridad y redes en un contexto de DevOps.

## **Requisitos previos:**
- Tener conocimientos básicos sobre redes (direcciones IP, puertos, protocolos).
- Conocer cómo instalar y usar herramientas en un entorno Linux o Ubuntu.

## **Tareas:**

### **Tarea 1: Investigación y Preparación**
1. **Investigación sobre Nmap:**
   - Investiga qué es Nmap y cómo se utiliza en la administración de redes y la seguridad informática.
   - ¿Qué tipos de escaneos puedes realizar con Nmap? (ej. escaneo de puertos, detección de versiones, identificación de sistemas operativos).
   - ¿Cuáles son los tipos de escaneos más comunes en Nmap, como **TCP Connect Scan**, **SYN Scan** y **UDP Scan**? Explica sus diferencias y cuándo usarlos.

2. **Instalación de Nmap:**
   - Instala Nmap en tu sistema Ubuntu. Si trabajas en un entorno de contenedores (Docker), también puedes instalarlo allí.
   - Verifica que la instalación sea correcta ejecutando `nmap --version` en la terminal.

### **Tarea 2: Escaneos Básicos**
1. **Escaneo de una Máquina Local:**
   - Realiza un escaneo básico de puertos en una máquina local de tu red con el comando:  
     `nmap <dirección IP>`
   - Analiza los puertos abiertos y los servicios detectados. ¿Qué descubriste sobre la máquina?

2. **Escaneo de Puertos Específicos:**
   - Realiza un escaneo para verificar si ciertos puertos específicos están abiertos en un servidor remoto (por ejemplo, SSH - puerto 22, HTTP - puerto 80, HTTPS - puerto 443). Utiliza el siguiente comando:  
     `nmap -p 22,80,443 <dirección IP>`
   - ¿Qué servicios están disponibles en esos puertos?

### **Tarea 3: Escaneos Avanzados**
1. **Detección de Versiones de Servicios:**
   - Realiza un escaneo para identificar las versiones de los servicios en ejecución usando:  
     `nmap -sV <dirección IP>`
   - ¿Por qué es importante saber qué versiones de servicios están corriendo? ¿Cómo puede esta información ayudar a mejorar la seguridad?

2. **Detección de Sistema Operativo:**
   - Realiza un escaneo para identificar el sistema operativo de la máquina objetivo con:  
     `nmap -O <dirección IP>`
   - ¿Cómo determina Nmap el sistema operativo y por qué esta información es útil?

### **Tarea 4: Pruebas de Seguridad**
1. **Escaneo de Vulnerabilidades:**
   - Investiga cómo realizar un escaneo para detectar vulnerabilidades usando los scripts NSE de Nmap. Utiliza el siguiente comando para detectar vulnerabilidades conocidas:  
     `nmap --script=vuln <dirección IP>`
   - Realiza el escaneo en un servidor de pruebas y describe las vulnerabilidades que se detectan.

### **Tarea 5: Documentación y Entrega**
1. **Informe Final:**
   - Redacta un informe detallado que incluya:
     - Respuestas a las preguntas de investigación.
     - Resultados de los escaneos realizados (puertos, servicios, versiones, sistema operativo, etc.).
     - Análisis de vulnerabilidades detectadas.
     - Se enviara a Slack el documento final

## **Evaluación:**
Tu proyecto será evaluado en base a los siguientes criterios:
- Complejidad y precisión en los escaneos realizados.
- Calidad y profundidad de la investigación sobre Nmap.
- Claridad y organización del informe final.
- Aplicación de conceptos de seguridad y redes.

---


