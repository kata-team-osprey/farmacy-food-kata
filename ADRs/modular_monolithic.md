# Design implementation using modular monolith architectural style

## Status
Accepted

## Context
There are multiple architectural styles to implement the architecture. As Farmacy Food is a startup just starting out to build the infrastructure, a cost effective strategy using limited resources will have to be used to implement the design and build out the infrastructure.

## Decision
The design will be implemented using modular monoliths because:
1. A small team can implement, build, test and design
2. Fosters increased reusability of the code

## Consequences
As a consequence of implementing modular monoliths, a small team will be able to develop, deploy and maintain the infrastructure and code. 
In the future, when the team grows and the needs of the team change to scale the operations, modular monolith will make it easier to implement and decompose the modules into a SOA or Microservices architectural style. 
Also,
1. Time to market will be faster due to all code updates/addition in a single repo.
2. Integration testing will be limited to testing between the modules and hence saving time and effort.
3. Security attack surface will be smaller as there are limited entry points into the system due to the nature of the architectural style.
