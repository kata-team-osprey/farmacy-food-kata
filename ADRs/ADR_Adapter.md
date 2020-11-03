# Use of adapters for communicating with POS and Smart Fridge

## Status
Accepted

## Context
End customers can purchase meals either from a Smart Fridge or a Kiosk equipped with a POS. 
Both these endpoints serve the same function but are different hardware and software systems.
The central system can access this via:
1. Single service but with different adapters
2. Single adapter per end system with sub-components that process messages into the system's queues 

## Decision   
Single adapter per end system with sub-components that process messages into the system's queues
1. encapsulating the APIs to each type of end system within the adapter
2. scalability - addition of more fridges and POS endpoints can scale up by adding more number of adapters
3. extensibility - addition of new types of end systems can extend by adding more types of adapters


## Consequences
The other components in the central system (that do not directly talk to end systems POS or Smart Fridge) 
are platform (POS/Smart Fridge) agnostic. The adapters in the  'Price Updater' abstracts out the end systems 
such that the 'Price Calculator' is unaware of the types of numbers of end systems.
