---
title: Pixora - Native Android App
description: Academic project | iOS application for exploring, organizing, and uploading visual content
slug: pixora-android
date: 2025-07-10 00:00:00+0000
image: pixora-android.png
categories:
    - Mobile Development
    - Android Development
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

Pixora is a native Android application developed as a Bachelor project for the Android Development subject of the Mobile Computing Master's program at Universidad Pontificia de Salamanca. The application is inspired by platforms like Pinterest and allows users to explore, organize, and share visual content.

## Features
The core functionalities of Pixora include:

- Browse and viewing images.   
- Searching for images.   
- Creating personalized lists (collections) to organize images.   
- Liking images.   
- Uploading your own photos from the camera or gallery.   
- Viewing your activity feed, including liked photos and photos added to lists.   
- Viewing your uploaded photos.
- Change app Language.

## Technical Details
The application was developed using modern Android technologies and best practices in software architecture:

- **Language and Framework**: Built entirely with Kotlin and Jetpack Compose, Google's modern declarative UI toolkit, for a more concise, intuitive, and efficient development process.   
- **Architecture**: A combination of MVVM (Model-View-ViewModel) and Clean Architecture was implemented to ensure a robust, scalable, and maintainable codebase. The project is clearly structured into Domain, Data, and Presentation layers.  
- **Data Management**: 
    -  **Room**: Used for local data persistence of structured data like photos, user-created lists, and activity logs. It was chosen for its compile-time query verification and seamless integration with Flow.
    - **Preferences DataStore**: Employed to store simple key-value data, such as user preferences for language and display mode (light/dark), offering a safe and asynchronous alternative to SharedPreferences.
- **API Integration**: The Unsplash API was integrated to provide a vast catalog of high-quality images. Network requests are managed efficiently using Retrofit for declarative API definition and OkHttp for handling connections.   
- **External Libraries**: Key third-party libraries were used to enhance functionality:
    - **Hilt**: For dependency injection, ensuring a decoupled architecture. It was chosen over Koin for its compile-time safety and official recommendation by Google.
    - **Coil (Coroutine Image Loader)**: For fast and efficient asynchronous image loading and caching, with native support for Jetpack Compose.   
    - **Lottie**: To render complex vector animations, used specifically for the initial splash screen.   
    - **Kotlinx Serialization**: Utilized to enable type-safe navigation with Jetpack Compose Navigation, allowing entire objects to be passed as arguments.  
- **Android Jetpack**: The application extensively uses components from Android Jetpack, including Navigation for managing app flow, Coroutines and Flow for asynchronous operations, and ViewModel for managing UI-related data.
- **Animations**: Various animations were included to improve the user experience, such as a Lottie animation on the splash screen, smooth visibility transitions for the navigation bar, and interactive animations for the "like" gesture.

## Publication
The application was published on the Google Play Store as a closed test version.
Link to the Google Play Store: [Pixora](https://play.google.com/store/apps/details?id=com.ibrepidevs.pixora)

## Project Repository
The source code for this project is available on GitHub: https://github.com/israelbrea12/Pixora-Android.git.

## View project in pdf
[Pixora-Android](/pixora-android.pdf)

## Video Pixora
{{< youtube "DYYbeGz09Fc" >}}