# generator-macchiato
Java backend service generator


This repo has the intend to create the ability to bootstrap fast a rest Java back-end service with less quesitons needed.
For that somethings will need to be default, as the `structured logs/Heroku and Travis configurations`.

___ 


To install the project:

`npm install -g generator-macchiato`

___ 

To run:

`yo macchiato`

___

To succefull run the project you will need:

- Git
- Gradle
- Docker
- Java 8
- Eclipse/IntelliJ

___

This project will create for you:
- The clock configuration to be able to inject Clock to LocalDate to be able to unit test.
- Gradle build file with configurations to support heroku/travis integrations as docker and postgres if you select this option.
- It will add the configuration to have Structure Logs with Logback, and Some aspects to help you log the application using MDC.

___

This is the structure that macchiato will generate:

```
project
│   .travis.yml
│   .gitignore
│   Procfile
│   build.gradle
└───gradle
│    └───scripts
│    │    │   java.gradle
│    │    │   spring-boot.gradle
│    │    │   postgres-docker.gradle
│    │    │   test.gradle
│
└───src/main/java/<%defaultPackage%>
│    │   Application.java
│    │
│    └───config
│    │    │   ClockConfiguration.java
│    │    │   PropertiesConfiguration.java
│    └───controller
│         │   GlobalExceptionHandler.java
│   
└───src/main/resources
│    │   application.properties
│    │   application-local.properties
│    │   logback.xml
│
└───src/test/java/<%defaultPackage%>
│    │   Application.java
│
└───src/test/resources
     │   application-test.properties
```

___