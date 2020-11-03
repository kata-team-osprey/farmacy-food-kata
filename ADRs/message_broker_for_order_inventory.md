# Common message broker to Order and Inventory Component

## Status
Accepted

## Context
The adaptors for communicating with POS and Smart Fridge system need to update the order and inventory details for the Order Component and Inventory component to display these details to the end users - namely Web, mWeb, Mobile website of Farmacy Foods and the Admin Portal.
The access to website will have to handle peak load during lunch hours.
Also the system should scale to support growth to thousands of users in a short period of time.

## Decision
We will use common message broker implementation to orchestrate the data adaptors for Order and Inventory data sources. This will remove the direct dependency between order and Inventory modules.
Also this will eliminate tight coupling between the Source Inventory/Order Adaptors and the Order/Inventory Modules providing better user experience by increasing the performance and availability of the system.

## Consequences
Using custom message brokers will allows us to:
1. Remove direct dependency between Order and Inventory modules and Inventory and Order processors.
2. Add fault tolerance on the single point of failure in accessing inventory and order data
3. As producers can add messages and consumers can process messages without interacting with each other, the primary components of Order, Inventory, Source Inventory and Source Order Processors will not be stalled waiting for each other, optimizing data flow.
