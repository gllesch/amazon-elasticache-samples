## Amazon ElastiCache Samples

Samples and documentation for using the [Amazon ElastiCache](https://aws.amazon.com/elasticache/) with [Redis](https://aws.amazon.com/elasticache/redis/) OSS compatibility and [Memcached](https://aws.amazon.com/elasticache/memcached/).

---

## Blogs

- [Online Feature Store](./blogs/feast-aws-credit-scoring/) Building online feature stores on AWS with Amazon ElastiCache with Redis OSS compatibility to support mission-critical ML use cases that require ultra-low latency and high throughput. [Build an ultra-low latency online feature store for real-time inferencing using Amazon ElastiCache with Redis OSS compatibility](https://aws.amazon.com/blogs/database/build-an-ultra-low-latency-online-feature-store-for-real-time-inferencing-using-amazon-elasticache-for-redis/)

## Hands-On Tutorials

The following are tutorials covering various use cases for [Amazon ElastiCache](https://aws.amazon.com/elasticache/).

- [Database Caching](./database-caching/) - Learn how to create a query cache for a relational database using Amazon ElastiCache with Redis OSS compatibility. In this tutorial, we take you through the process of deploying an [Amazon Relational Database Service](https://aws.amazon.com/rds/) RDS MySQL database and integrating an Amazon ElastiCache with Redis OSS compatibility cluster in front of the RDS instance in order to reduce query latency for often run MySQL queries.

- [Session Store](./session-store/) - Discover how to manage user sessions in a web-based application using Amazon ElastiCache with Redis OSS compatibility. In this tutorial, you will learn how to use ElastiCache with Redis OSS compatibility as a distributed cache for session management. You will also learn the best practices for configuring your ElastiCache nodes and how to handle the sessions from your application. 

- [Lambda Feature Store](./lambda-feature-store/) - Learn how Amazon ElastiCache can serve as the focal point for a custom-trained ML model to present recommendations to application and web users. Lambda functions are used to facilitate the interactions between ElastiCache with Redis OSS compatibility and Amazon S3. Then review how AWS Lambda interacts with Amazon ElastiCache with Redis OSS compatibility with insights loaded from a custom-built ML recommendation engine.

- [Spring Framework with GLIDE](./glide-samples/spring-framework-glide-example/) - See an example implementation of Spring Boot caching using the [Valkey GLIDE](https://github.com/valkey-io/valkey-glide) client.

## Webinars

- [Generative AI Virtual Assistant](./webinars/genai-chatbot/) - Build a generative AI Virtual Assistant with [Amazon Bedrock](https://aws.amazon.com/bedrock/), [Langchain](https://github.com/langchain-ai/langchain) and [Amazon Elasticache](https://aws.amazon.com/elasticache/). See [YouTube Video](https://www.youtube.com/watch?v=yWxDmQYelvg).

- [Flask Redis Session Management](./webinars/flask-redis-session/) - This is a simple Flask web application that demonstrates user session management using Redis as the session storage.

## DevOps

Deploy infrastructe as code

### AWS CDK [Cloud Development Kit]

#### TypeScript

- [Amazon ElastiCache Serverless for Memached](devops/aws-cdk/typescript/elasticache-serverless-memcached-minimal/README.md)
- [Amazon ElastiCache Serverless with Redis OSS compatibility](devops/aws-cdk/typescript/elasticache-serverless-redis-minimal/README.md)
- [Amazon ElastiCache with Redis OSS compatibility Cluster Mode Disabled](devops/aws-cdk/typescript/elasticache-redis-cmd/README.md)

---
## Tools 
Tools and documentation for using the [Amazon ElastiCache](https://aws.amazon.com/elasticache/)
[Serverless cost calculator] (tools/serverless-cost-calculator/README.md)

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.
