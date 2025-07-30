---
title: Pixora - Native iOS App
description: Academic project | iOS application for exploring, organizing, and uploading visual content
slug: pixora-ios
date: 2025-05-10 00:00:00+0000
image: pixora.png
categories:
    - Mobile Development
    - iOS Development
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

Pixora is a native iOS application developed as a Bachelor project for the iOS Development subject of the Mobile Computing Master's program at Universidad Pontificia de Salamanca. The application is inspired by platforms like Pinterest and allows users to explore, organize, and share visual content.

## Features
The core functionalities of Pixora include:

- Browse and viewing images.   
- Searching for images.   
- Creating personalized lists (collections) to organize images.   
- Liking images.   
- Uploading your own photos from the camera or gallery.   
- Viewing your activity feed, including liked photos and photos added to lists.   
- Viewing your uploaded photos.

## Technical Details
The application was developed using modern Apple technologies and architectural patterns:

- **Language and Framework**: Swift and SwiftUI were used for their safety, performance, and declarative UI capabilities.   
- **Architecture**: A combination of MVVM (Model-View-ViewModel) and Clean Architecture was implemented to ensure a robust, modular, and maintainable codebase. The project is structured into Domain, Data, and Presentation layers.   
- **Data Management**: Core Data was utilized for local data persistence, managing objects, and handling persistence, retrieval, validation, and change management.   
- **API Integration**: The Unsplash API was integrated to provide a large catalog of high-quality images for the application's content. Network requests were handled using URLSession.   
- **External Libraries**: Several external libraries were incorporated via Swift Package Manager to enhance functionality and user experience:
    - **CryptoSwift**: Used for generating MD5 hashes for API authentication.   
    **Lottie**: Integrated to display engaging animations on the Launch Screen.   
    **SDWebImageSwiftUI**: Used for asynchronous image loading and caching from URLs.   
    **Swinject**: Employed as a Dependency Injection framework to manage dependencies.   
- **Apple Frameworks**: Key native Apple frameworks were used:
    - **UserNotifications**: Implemented for managing local notifications to re-engage users.   
    - **AVFoundation**: Used for accessing the device's camera and capturing photos.   
    - **UIKit**: Utilized for functionalities not yet fully mature in SwiftUI, such as device information and integrating a camera preview (UIViewRepresentable).   
    - **Foundation**: Provided fundamental data types, collections, and system service access.   
- **Layout and Adaptability**: The layout was designed to be compatible with various iPhone and iPad screen sizes and orientations (vertical and horizontal) using GeometryReader, UIDevice, LazyVGrid with adaptive items, and size classes.   
**Animations**: Various animations were included to improve user experience, including a Lottie animation on the launch screen, tab bar visibility animations, and animations on the like and save buttons.

## Publication
The application was published on the Apple App Store on May 6, 2025.
Link to the App Store: [Pixora](https://apps.apple.com/es/app/pixora/id6745432045?l=en-GB)

## Project Repository
The source code for this project is available on GitHub: https://github.com/israelbrea12/Pixora-iOS.git.

## View project in pdf
[Pixora-iOS](/pixora-ios.pdf)

## Video Pixora
{{< youtube "4bGkxt8a2kE" >}}