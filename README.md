# spring-boot-initialzr-vanilla

A repository that contains what I got with a plain vanilla Spring Boot Initializr setup

I used the following options (basically, all of the defaults), on Monday 09/16/2019.

![screenshot](/IMAGES/spring-boot-initialzr-screen-shot.png)

I then unzipped the resulting demo.zip file into this repository.

Any changes subsequently made are documented in the git history of this repo.

#




 The Java files in this project

There are only two Java files in the very basic Spring-Boot Initializr demo.zip:

* `DemoApplication.java`  -- this is the `public static void main` of your project
* `DemoApplicationTests.java` -- this is the starting point for testing


# `DemoApplication.java`

The only imports we have are `SpringApplication` and `SpringBootAppllication`.

`@SpringBootApplication` is an annotation documented [here](https://docs.spring.io/spring-boot/docs/current/reference/html/using-boot-using-springbootapplication-annotation.html), although that documentation is not necessarily very enlightening on first read.   

But a short version is that it tells the Spring framework that we want the "auto-configuration magic" to happen for this class.  That auto-configuration magic includes a number of useful features such as connecting to databases automatically, using credentials that are defined in configuration files, without us having to write much code at all (if any!).   

The `SpringApplication` class has a static method called `run` that we can pass our own class to, passing through the command line arguments we were given, in order to run our application within the Spring framework.

So far, it isn't at all clear where we would put our own code to actually *do* anything.  But we'll get there.

```java
package com.example.demo;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class DemoApplication {

	public static void main(String[] args) {
		SpringApplication.run(DemoApplication.class, args);
	}

}
```

# DemoApplicationTests.java

This file has the starting point for writing tests for our application.  It starts out looking like this:

```java
package com.example.demo;

import org.junit.Test;
import org.junit.runner.RunWith;
import org.springframework.boot.test.context.SpringBootTest;
import org.springframework.test.context.junit4.SpringRunner;

@RunWith(SpringRunner.class)
@SpringBootTest
public class DemoApplicationTests {

	@Test
	public void contextLoads() {
	}

}
```

We'll return to what this code does later.