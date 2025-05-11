---
title: Pixora
description: Proyecto académico | Aplicación iOS para explorar, organizar y subir contenido visual
slug: pixora
date: 2025-05-10 00:00:00+0000
image: pixora.png
categories:
    - Desarrollo Móvil
    - Desarrollo iOS
tags:
    - Swift
    - SwiftUI
    - Xcode
    - Core Data
    - MVVM
    - Clean Architecture
    - Git, Github
    - Swinject
    - iOS

weight: 1       # You can add weight to some posts to override the default sorting (date descending)
---

Pixora es una aplicación nativa para iOS desarrollada como proyecto de fin de Grado para la asignatura de Desarrollo de Aplicaciones iOS del Máster Universitario en Informática Móvil de la Universidad Pontificia de Salamanca. La aplicación está inspirada en plataformas como Pinterest y permite a los usuarios explorar, organizar y compartir contenido visual.

## Características
Las funcionalidades principales de Pixora incluyen:

- Navegar y visualizar imágenes.
- Buscar imágenes.
- Crear listas (colecciones) personalizadas para organizar imágenes.
- Dar "Me gusta" a las imágenes.
- Subir tus propias fotos desde la cámara o galería.
- Ver tu feed de actividad, incluyendo fotos a las que has dado "Me gusta" y fotos añadidas a listas.
- Ver tus fotos subidas.

## Detalles Técnicos
La aplicación fue desarrollada utilizando tecnologías modernas de Apple y patrones arquitectónicos:

- **Lenguaje y Framework**: Se utilizaron Swift y SwiftUI por su seguridad, rendimiento y capacidades de UI declarativa.
- **Arquitectura**: Se implementó una combinación de MVVM (Model-View-ViewModel) y Clean Architecture para asegurar una base de código robusta, modular y mantenible. El proyecto está estructurado en capas de Dominio, Datos y Presentación.
- **Gestión de Datos**: Se utilizó Core Data para la persistencia local de datos, gestionando objetos y manejando la persistencia, recuperación, validación y gestión de cambios en esos datos.
- **Integración de API**: Se integró la API de Unsplash para proporcionar un amplio catálogo de imágenes de alta calidad para el contenido de la aplicación. Las peticiones de red se manejaron utilizando URLSession.
- **Librerías Externas**: Se incorporaron varias librerías externas a través de Swift Package Manager para mejorar la funcionalidad y la experiencia de usuario:
    - **CryptoSwift**: Utilizada para generar hashes MD5 para la autenticación de la API.
    - **Lottie**: Integrada para mostrar animaciones atractivas en la Launch Screen.
    - **SDWebImageSwiftUI**: Utilizada para la carga asíncrona y caché eficiente de imágenes desde URLs.
    - **Swinject**: Empleada como framework de Inyección de Dependencias para gestionar las dependencias.
- **Frameworks de Apple**: Se utilizaron frameworks nativos clave de Apple:
    - **UserNotifications**: Implementado para gestionar notificaciones locales para re-enganchar a los usuarios.
    - **AVFoundation**: Utilizado para acceder a la cámara del dispositivo y capturar fotos.
    - **UIKit**: Utilizado para funcionalidades aún no completamente maduras en SwiftUI, como información del dispositivo e integración de una vista previa de la cámara (UIViewRepresentable).
    - **Foundation**: Proporcionó tipos de datos fundamentales, colecciones y acceso a servicios del sistema.
- **Layout y Adaptabilidad**: El layout fue diseñado para ser compatible con varios tamaños de pantalla de iPhone y iPad, así como con las orientaciones vertical y horizontal, utilizando GeometryReader, UIDevice, LazyVGrid con ítems adaptativos y clases de tamaño.
- **Animaciones**: Se incluyeron varias animaciones para mejorar la experiencia de usuario, incluyendo una animación de Lottie en la pantalla de inicio, animaciones de visibilidad de la barra de pestañas y animaciones en los botones de "Me gusta" y "Guardar".

## Publicación
La aplicación fue publicada en la App Store de Apple el 6 de mayo de 2025.
Enlace a la App Store: [Pixora](https://apps.apple.com/es/app/pixora/id6745432045?l=en-GB)

## Repositorio del Proyecto
El código fuente de este proyecto está disponible en GitHub: https://github.com/israelbrea12/Pixora-iOS.git.

## Vídeo Pixora
{{< youtube "4bGkxt8a2kE" >}}