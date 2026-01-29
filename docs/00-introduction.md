# Gophermart - Introduction

This repository exists beacause i reached  a point where small crud projects stopped teaching me anything meaningful about backend engineering. And this is my attempt to build something that's a bit more complex to me.

## Why this project ?

I wanted a project that forces me to think about:
- service boundaries,
- contracts instead of func calls,
- intentional tradeoffs instead of 'the best practices'

E-commerce seems a very common project. But I believe it's very practical and 
teaches me real time complex scenarios that i need to be familiar with as a 
backend engineer. 

Also I'll  make it a little more challengeing to by adding edge cases and 
using a diff system design.

## Gophermart - A bit about this project

It's a distributed e-commerce sys built as a set of cooperating services.

At the grand scheme, it consists of :
- an API Gateway that is the system's public edge,
- a Product / Catalog service
- an Order service,
- a Payment and Notification service

A microservices str, each service owns its data, exposes explicit contracts, 
and communicates thru a well-defined interfaces.


## Why it's intentionally complex

A single database  would be easier to reason about.
A shared codebase would reduce boilerplate.

I chose not to do those on purpose.

The project is designed to surface:
- netword unreliability
- partial failures
- schema evolution
- service versioning

My thought is not making it just complex,
**I jsut wanted to understand how complex codebases work.**

## Final note
Gopermart will change.
Some ideas will trun out to be wrong.
Some pf my decisions will be revised or abandoned.

