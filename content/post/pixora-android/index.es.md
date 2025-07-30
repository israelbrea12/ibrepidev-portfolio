---
title: Pixora - Aplicación nativa Android
description: Proyecto académico | Aplicación Android para explorar, organizar y subir contenido 
slug: pixora-android
date: 2025-07-10 00:00:00+0000
image: pixora-android.png
categories:
    - Desarrollo Móvil
    - Desarrollo Android
tags:
    - Kotlin
    - Jetpack Compose
    - Room
    - Hilt
    - Retrofit
    - MVVM
    - Clean Architecture
    - Git
    - Github
    - Android

weight: 1       # You can add weight to some posts to override the default sorting (date descending)
---

Pixora es una aplicación nativa para Android desarrollada como proyecto para la asignatura de Desarrollo de Aplicaciones Android del Máster Universitario en Informática Móvil de la Universidad Pontificia de Salamanca. La aplicación está inspirada en plataformas como Pinterest y permite a los usuarios explorar, organizar y compartir contenido visual de una manera sencilla e intuitiva.

## Características
Las funcionalidades principales de Pixora incluyen:

- Navegar y visualizar imágenes filtradas por categorías.
- Buscar imágenes con una función de scroll infinito.
- Crear listas (colecciones) personalizadas para organizar fotos.
- Dar "Me gusta" a las imágenes para guardarlas en una sección de favoritos.
- Subir fotos propias desde la cámara o la galería del dispositivo.
- Ver un feed de actividad con las interacciones recientes, como "me gusta" y fotos añadidas a listas.
- Acceder a un perfil personal para ver las fotos subidas, las listas creadas y las imágenes favoritas.
- Cambiar el idioma.

## Detalles Técnicos
La aplicación fue desarrollada utilizando tecnologías modernas de Android y buenas prácticas de arquitectura de software:

- **Lenguaje y Framework**: Construida íntegramente con Kotlin y Jetpack Compose, el moderno toolkit de UI declarativa de Google, para un proceso de desarrollo más conciso, intuitivo y eficiente.
- **Arquitectura**: Se implementó una combinación de MVVM (Model-View-ViewModel) y Clean Architecture para asegurar una base de código robusta, escalable y fácil de mantener. El proyecto está claramente estructurado en capas de Dominio, Datos y Presentación.
- **Gestión de Datos**: 
    - **Room**: Utilizado para la persistencia local de datos estructurados como fotos, listas creadas por el usuario y registros de actividad. Se eligió por su verificación de consultas en tiempo de compilación y su integración nativa con Flow.
    - **Preferences DataStore**: Empleado para almacenar datos simples clave-valor, como las preferencias de idioma y modo de visualización (claro/oscuro), ofreciendo una alternativa segura y asíncrona a SharedPreferences.
- **Integración de API**: Se integró la API de Unsplash para proporcionar un amplio catálogo de imágenes de alta calidad. Las peticiones de red se gestionan de forma eficiente con Retrofit para la definición declarativa de la API y OkHttp para el manejo de las conexiones.
- **Librerías Externas**: Se utilizaron librerías clave de terceros para mejorar la funcionalidad:
    - **Hilt**: Para la inyección de dependencias, garantizando una arquitectura desacoplada. Fue elegido sobre Koin por su seguridad en tiempo de compilación y por ser la solución recomendada oficialmente por Google
    - **Coil (Coroutine Image Loader)**: Para la carga asíncrona y el almacenamiento en caché de imágenes de forma rápida y eficiente, con soporte nativo para Jetpack Compose.
    - **Lottie**: Para renderizar animaciones vectoriales complejas, utilizada específicamente en la pantalla de carga inicial (splash screen).
    - **Kotlinx Serialization**: Utilizada para habilitar una navegación type-safe con Jetpack Compose Navigation, permitiendo pasar objetos completos como argumentos.
- **Android Jetpack**: La aplicación utiliza extensivamente componentes de Android Jetpack, incluyendo Navigation para gestionar el flujo de la app, Coroutines y Flow para operaciones asíncronas, y ViewModel para la gestión de datos de la UI.
- **Animaciones**: Se incluyeron varias animaciones para mejorar la experiencia de usuario, como una animación de Lottie en la pantalla de carga, transiciones suaves de visibilidad para la barra de navegación y animaciones interactivas para el gesto de "me gusta".

## Publicación
La aplicación fue publicada en la Google Play Store como una versión de prueba cerrada.
Enlace a la Google Play Store: [Pixora](https://play.google.com/store/apps/details?id=com.ibrepidevs.pixora)

## Repositorio del Proyecto
El código fuente de este proyecto está disponible en GitHub: https://github.com/israelbrea12/Pixora-Android.git.

## Visualizar proyecto en pdf
[Pixora-Android](/pixora-android.pdf)

## Vídeo Pixora
{{< youtube "DYYbeGz09Fc" >}}