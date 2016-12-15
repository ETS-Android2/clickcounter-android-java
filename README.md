[![Build Status](https://travis-ci.org/LoyolaChicagoCode/clickcounter-android-java.svg?branch=master)](https://travis-ci.org/LoyolaChicagoCode/clickcounter-android-java)
[![codecov.io](https://codecov.io/github/LoyolaChicagoCode/clickcounter-android-java/branch/master/graph/badge.svg)](https://codecov.io/github/LoyolaChicagoCode/clickcounter-android-java)

# Learning Objectives

* Simple dependency injection
* Event-driven program execution
* State dependence in applications
* Mapping the model-view-adapter architecture to Android (and the command-line)
* Android application life cycle management (including rotation and back button)
* Playing a notification sound in Android
* Adapter pattern (wrapper, as opposed to the adapter in MVA)
* Dependency inversion principle (DIP)
* Automated unit and integration testing with JUnit
* Testcase Superclass pattern for xUnit testing
* Automated system testing by interacting with the GUI
* Automated GUI testing in Android

# Setting up the Environment

Check out the project using Android Studio. This creates the `local.properties` file
with the required line

    sdk.dir=<root folder of Android Studio's Android SDK installation>

# Running the Application

In Android Studio: `Run > Run app`

# Running the Tests

## Unit tests including out-of-emulator system tests using Robolectric

In Android Studio:

* `View > Tool Windows > Build Variants`
* `Test Artifact: Unit Tests`
* right-click on `app/java/edu.luc.etl.cs313 (test)`, then choose `Run Tests in edu.luc.etl.cs313`

You can also use Gradle:

    $ ./gradlew testDebug

You can view the resulting test reports in HTML by opening this file in your browser:

    app/build/reports/tests/debug/index.html

## Unit test code coverage

In Gradle:

    $ ./gradlew jacocoTestDebugUnitTestReport

You can view the resulting test reports in HTML by opening this file in your browser:

    app/build/reports/jacoco/jacocoTestDebugUnitTestReport/html/index.html

## Android instrumentation tests (in-emulator/device system tests)

In Android Studio:

* `View > Tool Windows > Build Variants`
* `Test Artifact: Android Instrumentation Tests`
* right-click on `app/java/edu...clickcounter (androidTest)`, then choose `Run Tests in edu...`

You can also use Gradle:

    $ ./gradlew connectedDebugAndroidTest
