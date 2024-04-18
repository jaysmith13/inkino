# inkino 
Flutter

## What is inkino?
inKino is a multiplatform Dart app for browsing movies and showtimes for Finnkino cinemas.

InKino showcases Redux, has an extensive set of automated tests and 40% code sharing between Flutter and web. The Android & iOS apps are made with a single Flutter codebase. The progressive web app is made with AngularDart. This project is generally something that I believe is a good example of a multiplatform Dart project.

## Folder Structure
There's three different folders. Each of them is a Dart project.

core: contains the pure Dart business logic, such API communication, Redux, XML parsing, sanitization, i18n, models and utilities. It also has a great test coverage.
mobile: this is the Flutter project. It imports core, and it's a 100% shared codebase for the native Android & iOS apps that go on app stores.
web: the AngularDart progressive web app. Also imports core, and it's the thing that is live at https://inkino.app.
To work on these projects, open each one of them in an editor of your choice.

For example, if you want to do a new feature and you do it for the Flutter project first, you'd open both core and mobile in separate editor windows. To clarify, you'd do File -> Open... for core and then File -> Open... again for mobile.

## Building the project
Renaming the TMDB configuration file
You don't need a TMDB API key, but the actor images won't load without it.

If you try to build the project straight away, you'll get an error complaining that a tmdb_config.dart file is missing. To resolve that, run this on your terminal in the project root:

cd core/lib/src && mv tmdb_config.dart.sample tmdb_config.dart && cd ../../..
OR

If you don't trust in random bash scripts copied from the Internet, you can just rename the tmdb_config.dart.sample to tmdb_config.dart manually.

Building from source
First, ensure that you followed the "Development environment setup" section above.

To run the web project, first run pub get initially, and then webdev serve in the root of the web project.
To run the Flutter project, open it in your editor and click the play button, or run flutter run on your terminal.

## Credit
Olli Haataja
