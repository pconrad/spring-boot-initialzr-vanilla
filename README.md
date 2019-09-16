# spring-boot-initialzr-vanilla

A repository that contains what I got with a plain vanilla Spring Boot Initializr setup

I used the following options (basically, all of the defaults), on Monday 09/16/2019.

![screenshot](/IMAGES/spring-boot-initialzr-screen-shot.png)

I then unzipped the resulting demo.zip file into this repository.

Any changes subsequently made are documented in the git history of this repo.

# What can you do with this code?

| Command | What it does   |
|----------|---------------------------------------|
| `mvn compile` | Should result in a clean compile |
| `mvn test` | Runs one sucessful test |
| `mvn package` | Builds the jar file `target/demo-0.0.1-SNAPSHOT.jar` |
| `java -jar target/demo-0.0.1-SNAPSHOT.jar` | If done after `mvn package`, runs the code to completion |

