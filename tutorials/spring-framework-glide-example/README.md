# Use Valkey GLIDE with Spring Boot

[Valkey Glide](https://github.com/valkey-io/valkey-glide) is the official open-source Valkey client library, proudly part of the Valkey organization.

[Spring Boot](https://docs.spring.io/spring-boot/index.html) helps you to create stand-alone, production-grade Spring-based applications that you can run. Spring Boot takes an opinionated view of the Spring platform and third-party libraries, so that you can get started with minimum fuss. It contains a [caching](https://docs.spring.io/spring-boot/reference/io/caching.html) component, making implementation of caching in your application quick and simple.

This demo will show you a simple way to implement the GLIDE client with Spring Boot caching.

## Prerequesites

To build the application, you must have the following prerequisites.

Some compute with the following installed:
- *Java 17* - To install the Java Development Kit (JDK) 17, run `sudo yum install -y java-17-amazon-corretto-devel` on your EC2 instance
- *Maven* - To install Apache Maven, run `sudo yum install -y maven` on your EC2 instance

The compute must have access to Redis OSS or Valkey. This can be an ElastiCache cluster, or run locally.

## Running

To run the demo application, update `application.properties` to point to Redis or Valkey.

`spring.data.valkey.host=cache1-XXXXX.serverless.euw2.cache.amazonaws.com`

Run `mvn spring-boot:run` in the root folder.

See the results!

## How it works

To use Valkey Glide, we add 2 classes to the application:

`SimpleValkeyGlideCache.java`. This class implements the Spring Framework Cache interface. It is simple in nature - all cache key objects must have the `toString()` method, and all cached objects must implement `java.lang.Serializable`. This class adapts Spring Framework to use the GLIDE client.

`ValkeyGlideCacheManager.java`. This class implements Spring Framework `org.springframework.cache.CacheManager` interface and instantiates a Bean Component. On startup, Spring Framework looks for a Bean implementing this interface and uses it to create and manage access to caches at runtime. This class uses `SimpleValkeyGlideCache` for caches.

The Maven POM file contains two dependencies:

```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-cache</artifactId>
</dependency>
<dependency>
    <groupId>io.valkey</groupId>
    <artifactId>valkey-glide</artifactId>
    <classifier>${os.detected.classifier}</classifier>
    <version>[1.0.0,2.0.0)</version>
</dependency>
```

`spring-boot-starter-cache` tells Spring Framework to implement caching.

`valkey-glide` includes the Valkey GLIDE client in your application. See the GLIDE [client documentation](https://valkey.io/clients/) for more details.

## Want to try this with your existing Spring Boot application?

1. Remove any existing Caching providers from your dependencies (i.e. `spring-boot-starter-cache-redis`).
2. Add `SimpleValkeyGlideCache.java` and `ValkeyGlideCacheManager.java` to your application.
3. Modify any entries in your `application.properties` that configure Redis, changing them to valkey (i.e. `spring.data.redis.host` becomes `spring.data.valkey.host`).

Give your application a try!





