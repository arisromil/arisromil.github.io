---
title: Reactive Patterns
date: 2024-03-03 00:00:00 0000
categories: [reactive]
tags: [patterns]     # TAG names should always be lowercase
---

## Fault Tolerance and Recovery Patterns
- Simple Component - component should do only one thing but do it in full
- Error Kernel  - In a supervision heirarchy, keep important application state or functionality near the root while delegating risky operations towards the leaves
- Let-It-Crash - Prefer a full component restart to internal failure handling
- Circuit Breaker - Protect services by breaking the connection to their users during prolonged failure conditions
	
## Replication Patterns
- Active-Passive - Keep multiple copies of the service running in different locations, but only accept modifications to the state in one location at any given time
- Multiple-Master - Keep multiple copies of a service running in different locations, accept modifications everywhere, and disseminate all modifications among them
- Active–Active - Keep multiple copies of a service running in different locations, and perform all modifications at all of them
	
## Resource-management Patterns
- Resource Encapsulation - A resource and its lifecycle are responsibilities that must be owned by one component
- Resource Loan - Give a client exclusive transient access to a scarce resource without transferring ownership
- Complex Command - Send compound instructions to the resource to avoid excessive network usage
- Resource Pool - Hide an elastic pool of resources behind their owner
	 
## Message flow Patterns
- Request–Response - Include a return address in the message to receive a response
- Self-Contained Message - Each message will contain all information needed to process a request as well as to understand its response
- The Ask - Delegate the handling of a response to a dedicated ephemeral component
- The Forward Flow - Let the information and the messages flow directly toward their destination where possible
- The Aggregator - Create an ephemeral component if multiple service responses are needed to compute a service call’s result
- The Saga - Create an ephemeral component to manage the execution of a sequence of actions distributed across multiple components
- Business Handshake - Include identifying and/or sequencing information in the message, and keep retrying until confirmation is received
	
## Flow control Patterns
- The Pull - Have the consumer ask the producer for batches of data
- The Managed Queue - Manage an explicit input queue, and react to its fill level
- The Drop - Dropping requests is preferable to failing uncontrollably
- The Throttling - Throttle your own output rate according to contracts with other services
	
## State management and persistence Patterns
- The Domain Object - Separate the business domain logic from communication and state management
- The Sharding - Scale out the management of a large number of domain objects by grouping them into shards based on unique and stable object properties
- The Event-Sourcing - Perform state changes only by applying events. Make them durable by storing the events in a log.
- The Event Stream -  Publish the events emitted by a component so that the rest of the system can derive knowledge from them