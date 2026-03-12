# AWS Secure Infrastructure Lab

## Objetivo
En este proyecto he diseñado y desplegado una infraestructura segura en AWS para practicar conceptos de ciberseguridad cloud.  
El laboratorio incluye segmentación de red, control de accesos, monitorización y detección de amenazas.

## Arquitectura
- **VPC:** CyberLab-VPC (10.0.0.0/16)
- **Subred pública:** Public-Subnet (10.0.10.0/24)
- **Subred privada:** Private-Subnet (10.0.20.0/24)
- **EC2 Web Server:** instancia Amazon Linux, puerto 80 abierto al público, SSH solo desde mi IP
- **Security Group:** controla acceso a puertos 22 y 80
- **CloudTrail:** registra todas las acciones de AWS
- **S3:** almacenamiento seguro de logs
- **GuardDuty:** detección de actividad sospechosa

## Pasos realizados
1. Creación de VPC y subredes (pública y privada) para segmentación de red
2. Configuración de Internet Gateway y tabla de rutas pública
3. Despliegue de EC2 con acceso controlado mediante Security Group y Key Pair SSH
4. Instalación de servidor web Apache
5. Activación de CloudTrail para auditoría de eventos
6. Configuración de S3 para almacenamiento de logs
7. Activación de GuardDuty para detección de amenazas
8. Simulación de ataques (SSH fallidos y escaneo de puertos) y observación de findings

## Lecciones aprendidas
- Importancia de la segmentación de red y control de accesos
- Cómo configurar un EC2 de forma segura
- Uso de CloudTrail y S3 para auditoría
- Monitorización y detección de amenazas con GuardDuty
- Simulación de ataques y análisis de resultados
