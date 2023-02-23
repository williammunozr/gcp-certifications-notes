# App Engine

App Engine is a PaaS compute service that provides a managed platform for running applications.

## Features

- When you use `App Engine`, your focus is on your application and not on the VMs (`infrastructure`) that run the application.
- Instead of configuring VMs, you specify some basic resource requirements along with your application code, and Google will manage the resources needed to run the code.
- Users have less to manage, but also have less control over the compute resources that are used to execute the application.
- App Engine is created within a project.
- The number of instances used to provide an application depends on your configuration for the application and the current load on the application.
- Google manages the scale-in and scale-out according to the application load. This kind of autoscaling is available with `dynamic instances`.

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