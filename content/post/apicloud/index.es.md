---
title: Creación de una API con Express y despliegue en la nube con AWS
description: Proyecto académico | Desarrollo de una API REST con Express, autenticación JWT, SQLite y despliegue en AWS con Packer y Terraform
slug: api-express-aws
date: 2025-03-10 00:00:00+0000
image: apicloud.png
categories:
    - Desarrollo Backend
    - Cloud Computing
tags:
    - Node.js
    - Express
    - API REST
    - JWT
    - SQLite
    - AWS
    - EC3
    - RDS
    - Packer
    - Terraform

weight: 1
---

Este proyecto fue desarrollado como parte de la asignatura de Tecnologías del lado del servidor: Cloud Computing dentro del Máster Universitario en Informática Móvil (MIMO). El objetivo fue implementar una API REST completa utilizando **Node.js y Express**, con autenticación mediante **JWT**, persistencia en **SQLite** y despliegue en **AWS** siguiendo buenas prácticas de escalabilidad y automatización.

## Objetivos del proyecto

- Implementar una API REST conforme a una especificación **OpenAPI**.
- Gestionar autenticación y autorización con **JWT**.
- Implementar operaciones **CRUD** para los recursos de películas y valoraciones.
- Aplicar validaciones de datos y manejo adecuado de códigos de estado HTTP.
- Desplegar la API en **AWS** con una infraestructura escalable y automatizada usando **Packer** y **Terraform**.

## Funcionalidades principales

### 1. Autenticación y seguridad

- **Endpoint de login** (`POST /sessions`) para generar tokens JWT.
- Protección de rutas sensibles mediante **middleware de autenticación**.
- Manejo de errores de autenticación con respuestas adecuadas (`401 Unauthorized`).

### 2. Gestión de películas (`/movies`)

- **GET /movies**: Devuelve todas las películas con los campos requeridos (ID, título, género, duración, rating).
- **Paginación opcional** para mejorar la eficiencia en consultas grandes.
- **Manejo de errores** con respuestas adecuadas (`404 Not Found`, `500 Internal Server Error`).

### 3. Gestión de valoraciones (`/ratings`)

- **CRUD completo** para que los usuarios puedan crear, leer, actualizar y eliminar valoraciones.
- **Validaciones**:
  - `rating` debe estar entre **0 y 5**.
  - `comentarios` con máximo **500 caracteres**.
- **Restricciones de acceso**:
  - Solo usuarios autenticados pueden modificar o eliminar sus valoraciones.
  - Manejo de errores con códigos adecuados (`401 Unauthorized`, `422 Unprocessable Entity`, `201 Created`).

### 4. Gestión de la lista de películas por ver (`/watchlist`)

- Permite a los usuarios añadir y gestionar películas pendientes de ver.
- Validación de **IDs de películas** antes de añadirlas.
- Manejo de estados de películas vistas/no vistas.
- **Respuestas adecuadas**:
  - `409 Conflict` para películas duplicadas.
  - `422 Unprocessable Entity` para IDs inválidos.
  - `404 Not Found` para películas inexistentes.

## Implementación técnica

### **Tecnologías utilizadas**
- **Node.js + Express**: Desarrollo de la API REST.
- **SQLite**: Base de datos ligera y eficiente.
- **JWT (jsonwebtoken)**: Implementación de autenticación.
- **Docker**: Contenerización del entorno de desarrollo.
- **AWS (EC2, S3, IAM)**: Infraestructura en la nube.
- **Packer**: Creación de imágenes AMI para AWS.
- **Terraform**: Automatización del despliegue en la nube.

### **Persistencia y base de datos**
- Uso de **SQLite** para almacenar información de usuarios, películas y valoraciones.
- **Migraciones y esquema definido** para garantizar la integridad de los datos.
- **ORM Sequelize** para facilitar la gestión de la base de datos.

### **Despliegue en AWS**

#### **1. Creación de AMI con Packer**
Se generó una **Amazon Machine Image (AMI)** con la configuración necesaria para ejecutar la API:
- Instalación de **Node.js** y dependencias.
- Configuración del entorno y variables necesarias.
- Creación de un script para la ejecución automática del servicio.

#### **2. Infraestructura con Terraform**
Se implementó la infraestructura con **Terraform**, asegurando escalabilidad y automatización:
- **Instancia EC2** configurada con la AMI generada.
- **Balanceador de carga** para distribuir el tráfico.
- **Auto Scaling Group** para aumentar o reducir instancias según demanda.
- **Almacenamiento en RDS** para persistencia de datos en la nube.
- **Gestión de IAM roles y permisos** para garantizar la seguridad.

### **Automatización y escalabilidad**
- **Infraestructura autoscalable** que permite ajustar el número de instancias en función de la carga.
- **Manejo de errores** para garantizar alta disponibilidad y minimizar tiempos de inactividad.
- **Persistencia de datos** asegurada con almacenamiento en AWS.

## Conclusiones y aprendizajes
Este proyecto permitió consolidar conocimientos en **desarrollo backend con Express**, autenticación JWT, bases de datos **SQL**, así como en **infraestructura cloud y automatización del despliegue** en AWS. Se aplicaron buenas prácticas de seguridad, validaciones de datos y manejo de errores, logrando un sistema robusto y escalable.

## Recursos y código fuente
- [Repositorio en GitHub](https://github.com/israelbrea12/Despliegue-API-express-AWS.git)
- [Documentación OpenAPI](/mimo_movies.yaml)

