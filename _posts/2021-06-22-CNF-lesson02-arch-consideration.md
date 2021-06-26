---
toc: false
layout: post
hide: false
search_exclude: false
comments: true
description: Difference between monoliths and microservices and when to use each one.
categories: [SCNF]
title: Architecture Considerations for Cloud Native Applications
---

There are two main approaches to design and build application which are referred to as **Monoliths** and **microservices**. it is very critical to think about the approach to follow before starting the design and the coding process to avoid unnecessary pullbacks.

The context discovery process helps in defining the overall structure and design of the components that can enable adding new features with minimum engineering effort.

## discovery process

The main steps in the discovery process are :

1- list functional requirements (what services should the application deliver)

- Who are the stakeholders and what are their needs
- What functionalities are required and what are the ones that are nice to have
- Who are the end users and how will they interact with the application 
- What are the Input and output processes in the application

2- list all available resource that helps in the implementation

- Engineering resources
- Financial resources
- Time frames
- Internal knowledge

## Application tires and their relation to the architecture 

Each application consists of 3 main tires:

- UI (User Interface) - handles HTTP requests from the users and returns a response
- Business logic - contained the code that provides a service to the users
- Data layer - implements access and storage of data objects

When working with a monoliths or microservices approach, the 3 tires are treated differently

**Monoliths**

In a monolithic architecture, application tiers can be described as:

- part of the same unit
- managed in a single repository
- sharing existing resources (e.g. CPU and memory)
- developed in one programming language
- released using a single binary

**Microservices**

In a microservices architecture, application tiers are managed independently, as different units. Each unit has the following characteristics:

- managed in a separate repository
- own allocated resources (e.g. CPU and memory)
- well-defined API (Application Programming Interface) for connection to other units
- implemented using the programming language of choice
- released using its own binary

Choosing and architecture is highly dependent on the functional requirements such as product features dependencies and the available resources es such as the engineering team. 

If an organization have large resources and powerful engineering force they can go with micro services but if they have time limits or few resources or small team a monolith approach is usually taken.

## Trade-offs for Monoliths and Microservices

There is no right or wrong choice it all depends on the trade-offs associated with with each architecture in terms of development complexity, scalability, time to deploy, flexibility, operational cost, and reliability

### Development Complexity

Development complexity represents the effort required to deploy and manage an application.

**Monoliths** - one programming language; one repository; enables sequential development

**Microservice** - multiple programming languages; multiple repositories; enables concurrent development

### Scalability
Scalability captures how an application is able to scales up and down, based on the incoming traffic.

**Monoliths** - replication of the entire stack; hence it's heavy on resource consumption

**Microservice** - replication of a single unit, providing on-demand consumption of resources

### Time to Deploy

Time to deploy encapsulates the build of a delivery pipeline that is used to ship features.

**Monoliths** - one delivery pipeline that deploys the entire stack; more risk with each deployment leading to a lower velocity rate

**Microservice** - multiple delivery pipelines that deploy separate units; less risk with each deployment leading to a higher feature development rate

### Flexibility

Flexibility implies the ability to adapt to new technologies and introduce new functionalities.

**Monoliths** - low rate, since the entire application stack might need restructuring to incorporate new functionalities

**Microservice** - high rate, since changing an independent unit is straightforward

### Operational Cost
Operational cost represents the cost of necessary resources to release a product.

**Monoliths** - low initial cost, since one code base and one pipeline should be managed. However, the cost increases exponentially when the application needs to operate at scale.

**Microservice** - high initial cost, since multiple repositories and pipelines require management. However, at scale, the cost remains proportional to the consumed resources at that point in time.

### Reliability

Reliability captures practices for an application to recover from failure and tools to monitor an application.

**Monoliths** - in a failure scenario, the entire stack needs to be recovered. Also, the visibility into each functionality is low, since all the logs and metrics are aggregated together.

**Microservice** - in a failure scenario, only the failed unit needs to be recovered. Also, there is high visibility into the logs and metrics for each unit.


## Best Practices For Application Deployment

There are basic best practices when it comes to deploying an application regardless if it is a monoliths or microservices application. These practices help in improving the lifecycle of the application and make it easier to maintain and improve upon later. Here is the list of best practices:

**1- Health Checks:** it showcase the status of an application. These checks report if an application is running and meets the expected behavior to serve incoming traffic

**2- Metrics:** Statistics to quantify the performance of the application such as as number of active users, number of requests per seconds, longest/average response time for a request, resources (CPU, RAM ...) utilization etc.

**3- Logs:** provides valuable insights into what operations a service is performing at a point in time which can have multiple levels (DEBUG, INFO, WARN, ERROR, FATAL)

**4- Tracing:** creating a full picture of how different services are invoked to fulfill a single request

**5- Resource Consumption:** encapsulates the resources an application requires to be fully operational such as CPU, RAM, Network throughput etc.

## Amorphous Applications

Applications are in a constant state of change and during the lifecycle of an application it might have operations applied to it during application maintenance such as

- Split: when a functionality is too big or complex and it needs to be split into smaller units.
- Merge: when a unit is very granular or apply only to handful of cases it might be good to merge it with another unit.
- replace: sometimes a junctional is replaced entirely by a new process or written in a new framework or programing language to address issues such as performance or maintainability or extensibility.
- Stale: when a functionality or unit is no longer needed by the business or the application it is retired.

