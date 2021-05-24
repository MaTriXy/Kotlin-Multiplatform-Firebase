# Kotlin Multiplatform Firebase.

[![Build Status](https://travis-ci.org/RubyLichtenstein/Kotlin-Multiplatform-Firebase.svg?branch=master)](https://travis-ci.org/RubyLichtenstein/Kotlin-Multiplatform-Firebase)
[![Kotlin](https://img.shields.io/badge/kotlin-1.3.0-blue.svg)](http://kotlinlang.org)


### Kotlin is everywhere!

This project demonstrates the benfits of kotlin multiplatform by implementating a multiplatform mobile application (Android/iOS) with firebase as a backend (Node.js) all in kotlin.

The application is using Firestore to store a list of posts and firebase functions to send notifications for new posts. 

## Modules.

- `common-all` - Multiplatform Module - shared code between clients/server.
- `common-client` - Multiplatform Module - shared code between clients (Android/iOS). 
- `firebase` - Node.Js app.
- `android` - Android app.
- `iOS` - iOS app.

![modules_diagrams](https://github.com/RubyLichtenstein/Kotlin-Multiplatform-Firebase/blob/master/diagrams/modules.svg)



## Project Architecture

![modules_diagrams](https://github.com/RubyLichtenstein/Kotlin-Multiplatform-Firebase/blob/master/diagrams/arch.svg)

### `common-all`

#### Clients/Server shared code.
- Data Models.
- Repositories.

### `common-client`

#### Clients shared code.
- Presenters. 

#### Platform specific code.
- Views.

## Testing

### Testing libraris
Common module testing.
https://github.com/mockk/mockk

### JVM

### JS

Jest https://jestjs.io/

### Native
//TODO 

## Build run and test. 

### Setup
1. Clone this project.
2. enable kotlin 1.3 (https://proandroiddev.com/setup-kotlin-eap-in-your-android-app-73f2c06308e5)

- if you're using the canary version of Android Studio
 check if kotlin 1.3 plugin is enabled for your version
 
 https://plugins.jetbrains.com/plugin/6954-kotlin

#### Running the Android app.
`./gradlew android:app:installDebug`

#### Running the iOS app.
//TODO

#### Running the Node.js App (deploy to Firebase)

1. `cd firebase/functions`
2. ` npm install`
3. `./gradlew common-all:firebaseDeploy`

#### Testing the Node.js App.
- `./gradlew common-all:firebaseTest`

## Libraries used in this project

#### common

- Serialization https://github.com/Kotlin/kotlinx.serialization
- Multiplatform Settings https://github.com/russhwolf/multiplatform-settings
- mockk https://github.com/mockk/mockk
