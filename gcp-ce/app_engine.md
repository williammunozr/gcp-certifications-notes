# App Engine

App Engine is a PaaS compute service that provides a managed platform for running applications.

## Features

- When you use `App Engine`, your focus is on your application and not on the VMs (`infrastructure`) that run the application.
- Instead of configuring VMs, you specify some basic resource requirements along with your application code, and Google will manage the resources needed to run the code.
- Users have less to manage, but also have less control over the compute resources that are used to execute the application.
- App Engine is created within a project.
- The number of instances used to provide an application depends on your configuration for the application and the current load on the application.
- Google manages the scale-in and scale-out according to the application load. This kind of autoscaling is available with `dynamic instances`.
- App Engine also provides `resident instances`. You can add or remove resident instances manually.
- 

## App Engine Standard and Flexible Environments

`App Engine` provides two types of runtime environments:

- Standard.
- Flexible.

### App Engine Standard Environment

- The `standard` environment is the original `App Engine` environment.
- It consists fo a preconfigured, language-specific runtime.
- There are two generations of the `standard` environment.
- The `second generation` improves on the performance of the first generation and has fewer limitations.

#### App Engine Standard Supported Languages

- First Generation:
  - Python 2.7
  - Java 8
  - PHP 5.5Go 1.11
- Second Generation:
  - Python 3
  - Java 11, 17
  - Node.js
  - PHP 7/8
  - Go 1.12+

#### Second Generation

- Developers can use any language extension, but in the first generation only a select set of extensions and libraries are allowed.
- Network access is restricted in the first generation, but users have full network access in the second generation.
- App Engine services are scaled using automatic, manual, or basic scaling.
- App Engine service gets compute and memory resources based on the instance class configured for the service.

### App Engine Flexible Environment

- App Engine `Flexible` Environment provides more options and control to developers who would like the benefits of a platform as a service (PaaS) like App Engine but without the language and customization constraints of the App Engine Standard Environment.
- Uses containers as the basic building block abstraction.
- Users can customize their runtime environments by configuring a container.
- The `Flexible` environment uses `Docker` containers.

## App Engine Use Cases

- Is a good choice for a computing platform when you have little need to configure and control the underlying operating system or storage system.
- App Engine manages underlying VMs and containers and relieves developers and DevOps of some common system administration tasks, like patching adn monitoring servers.

### When to use App Engine Standard Environment

- Design for applications written in one of the supported languages.
- The standard environment provides a language-specific runtime that comes with its own containers.

### When to use App Engine Flexible Environment

- Is well suited for applications that can be decomposed into services and where each service can be containerized.

