# 🚀 JWT Auth Example

JWT-based Spring security REST API.

## Technology stack

java 21, Spring Boot, JPA, Security

## Prerequisites

The following items should be installed in your system:

- java 21 or newer.
- git command line tool (https://help.github.com/articles/set-up-git)
- Your preferred IDE (IDEA preferably)

## Database configuration

Application uses a MySQL as a persistent storage. Options to get it up:

1. Use remote existing mysql. It is needed to specify the path in configs.
1. Start local mysql in docker `docker compose -f compose.yaml up -d`

### Running locally

This application is a [Spring Boot](https://spring.io/guides/gs/spring-boot) application built
using [Maven](https://spring.io/guides/gs/maven/). You can build a jar file and run it from the command line:

```
git clone https://github.com/iqkv/quickstart-jpa-jwt-secured.git
cd quickstart-jpa-jwt-secured
./mvnw package
java -jar target/*.jar
```

You might also want to use Maven's `spring-boot:run` goal - applications run in an exploded form, as they do in your IDE:

```
./mvnw spring-boot:run -Dspring-boot.run.profiles=local -P dev
```

Now you can access to the Swagger UI here: http://localhost:8080/swagger-ui.html

### Working with Application in your IDE

1. On the command line

```
git clone https://github.com/iqkv/quickstart-jpa-jwt-secured.git
```

2. Inside IDE

In the main menu, choose `File -> Open` and select the Application [pom.xml](pom.xml). Click on the `Open` button.
Activate "local" profile in the Run settings or set it via environment
variables. [instruction](https://stackoverflow.com/questions/38520638/how-to-set-spring-profile-from-system-variable)
Wait to indexing completion and push the green "play" button.

3. Navigate to Swagger UI

Visit [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html) in your browser.

## Code conventions

The code follows [Google Code Conventions](https://google.github.io/styleguide/javaguide.html). Code
quality is measured by:

- Sonarqube
- [PMD](https://pmd.github.io/)
- [CheckStyle](https://checkstyle.sourceforge.io/)
- [SpotBugs](https://spotbugs.github.io/)
- [Qulice](https://www.qulice.com/)

### Tests

This project has standard JUnit tests. To run them execute this command:

```text
./mvnw verify -Puse-qulice
```

It is mandatory to keep test code coverage not below **80** percents and cover all business logic and edge cases.

## Versioning

Project uses a three-segment [CalVer](https://calver.org/) scheme, with a short year in the major version slot, short month in the minor version slot, and micro/patch version in the third
and final slot.

```
YY.MM.MICRO
```

1. **YY** - short year - 6, 16, 106
1. **MM** - short month - 1, 2 ... 11, 12
1. **MICRO** - "patch" segment
