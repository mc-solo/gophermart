# Problem Statement

Modern backend systems rarely fail because of bad algorithms. 
They fail becuase of multiple independent part must cooperate under unreliable conditions.

---

## The core problem

In a distributed system:

- network calls can fail or timeout
- services can be unavailable while others remain healthy
- data can be temporarily inconsistent
- retries can cause duplication

What I'm trying to address is
 **how to model and coordinate these workflows without relying on global state, synchrounous execution, or perfect reliablity**

---

## Why simple solutions fail

A single-service or tightly coupled system works well at small scale, but begins to break down when:

- different parts of the system need to scale independently
- teams own different domains and deploy at different times
- failures must be isolated instead of cascading
- data ownership needs to be clearly defined

---

## Business workflows under failure

A typical order flow involves:
- validating product availability
- creating an order
- reserving inventory
- processing payment
- sending notifications

In a distributed architecture, each of these steps may succeed or fail independently.

The system must handle scenarios where:
- an order is created but payment fails
- payment succeeds but notification fails
- a service becomes unavailable mid-workflow
- retries introduce duplicate requests


## I'm assuming the following conditions

- services are independently deployable
- each service owns its own data
- inter-service communication is unreliable by default
- failure is a normal operating condition

**I'm trying my best to reflect real prod environment rather than idealized system.**

The result sys might not be perfect but i will explain when asked :)