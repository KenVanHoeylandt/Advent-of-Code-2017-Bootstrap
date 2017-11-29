# Advent of Code 2017

## Introduction

This repository contains a Kotlin bootstrap project for Advent of Code 2017. It also comes with an optional RxJava2 dependency.

The project fetches the data for each day from the server, provided that you start it with the required session token (see explanation below). The data is cached, to ensure fast subsequent runs of your application.

## Running the application

To start fetching assignments for your project, you need to get a session token to authenticate.

To do this, use your the developer tools of your web browser:

 - Go to [AdventOfCode.com](https://adventofcode.com)
 - Login
 - Open the developer tools of your browser (on Safari and Firefox for macOS you can press `CMD` + `Alt` + `I`.)
 - Switch to the networking tab of the developer tools
 - Reload the page
 - Find the session key in the headers from one of the requests

### Commandline

Building the jar file:

```
./gradlew jar
```

Running the jar file:

```
java -jar build/libs/AdventOfCode2017.jar [sessionToken] [day]
```

A session token can be fetched by logging in on your browser and debugging the browser request.

### IntelliJ IDEA

Create a new run configuration and enter the following data:

![screenshot](docs/intellij_application_dialog.png)

## Creating solutions

The bootstrap template only contains the classes to start with day 1.

To add a new day, you need to create a new `Solution` class and append it to the `Application.solutions` array field.
