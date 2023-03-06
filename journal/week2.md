# Week 2 — Distributed Tracing

What is Distributed Tracing and how it is different form Observability?

*Distributed tracing is a specific technique for tracking requests through a distributed system, while observability is a broader concept that includes various techniques and tools for understanding and troubleshooting complex systems*

> 📝 *Throughout the course of this week, I acquired knowledge on distributed tracing and its implementation using various platforms such as Honeycomb, AWS X-Ray, and Rollbar. Additionally, I successfully configured Cloudwatch to monitor the traces within the application.*

## Instrument backend flask application to use Open Telemetry (OTEL) with Honeycomb.io as the provider

What is Open Telemetry?

*It is a set of tools and best practices for collecting and exporting <ins> telemetry data</ins> from applications*

>**Note** 
>
>**In software development, telemetry refers to the collection of data about the performance, health, and usage of an application or service, which can be used for monitoring, debugging, and optimization purposes.**

What is HoneyComb?

*Honeycomb is a cloud-based observability and debugging platform used to collect, analyze, and visualize telemetry data such as logs, traces, and metrics in real-time*

Successfully instrumented HoneyComb in backend flask app - 🔗 [Instrumented honeycomb in backend](https://github.com/snehpalkaur/aws-bootcamp-cruddur-2023/commit/17f14df7f10d9e01cba3aca8a4379af69a7f7078)


## Implementation of Rollbar

What is Rollbar?

*Rollbar is a cloud-based error tracking and debugging platform that detects and reports errors, exceptions, and crashes in real-time to help developers quickly identify and resolve issues. It provides integrations with third-party tools and services for further analysis and notification.*

Successfully instrumented Rollbar for Error Logging - 🔗 [Instrumented Rollbar](https://github.com/snehpalkaur/aws-bootcamp-cruddur-2023/commit/07171a37ca092070c9fc042491298619d0cfaccf)

## Instrument AWS X-Ray into backend flask application

What is AWS X-ray?

*AWS X-Ray is a distributed tracing system for cloud-based applications that allows developers to identify performance issues and errors in their microservices-based architectures. It provides visualization and analysis tools and is fully integrated with other AWS services.*

Implemented AWS X-ray into backend flask-app - 🔗 [Instrumented AWS X-ray](https://github.com/snehpalkaur/aws-bootcamp-cruddur-2023/commit/214308e4f5300fb53e0458f124eb668d317012c4)

## Install WatchTower and write a custom logger to send application log data to CloudWatch Log group

🔗 [Implemented Cloudwatch](https://github.com/snehpalkaur/aws-bootcamp-cruddur-2023/commit/80a38b6f50ce8d4f707b6630cc1e13b4fdadfb52)


## Instrumentation to Honeycomb to add more attributes eg. UserId, Add a custom span
🔗 [Added a custom span](https://github.com/snehpalkaur/aws-bootcamp-cruddur-2023/commit/b19b15b9ecf56a86aa66aaeb31785efc8a4d0653)
