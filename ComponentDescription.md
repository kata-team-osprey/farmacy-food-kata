# Component Description

The list of major logical components in system. Consumers, publishers, and API layers are out of scope.

## User Profile Manager
Provides Login and Registration Flows.
Uses DB to store user profiles including Food preferences.
Saving of other metadata like addresses, credit cards, etc.

### Actions for Actors
| Actor      | Actions |
| :---        |    :---   |
| Customer | Manages their profile 

## Inventory Manager

Uses DB to store current inventory for locations.

### Actions for Actors
| Actor      | Actions |
| :---        |    :---   |
| Customer | Searches inventory by locations |
| Kitchen Admin | Searches inventory by locations |

## Orders

Uses DB to store current orders and order history.

### Actions for Actors
| Actor      | Actions |
| :---        |    :---   |
| Customer | Makes new order |
| Customer | Looks up orders history |
| Kitchen Admin | Looks up orders history |
| System | Matches new purchases with orders made |

## Promotions & Coupons

Uses DB/Rule Engine to store rules for promotions, including generated coupons.

### Actions for Actors
| Actor      | Actions |
| :---        |    :---   |
| Kitchen Admin | Manages discount rules |
| System | Starts promotions, generates coupoons |

## Menu Catalog

Uses DB to store information about menu items that are sold with base/default prices.

### Actions for Actors
| Actor      | Actions |
| :---        |    :---   |
| Kitchen Admin | Manages menu items |

## Feedback system

Uses DB to store review requests and customer reviews.

### Actions for Actors
| Actor      | Actions |
| :---        |    :---   |
| Customer | Provides feedback on purchases |
| System | Tracks purchases for reviews to be made |

## Price Calculator

Does not store any information. Used for application of promotion rules.

### Actions for Actors
| Actor      | Actions |
| :---        |    :---   |
| Customer | Display prices with applied coupons |

## Price Tracker

Does not store any information.

### Actions for Actors
| Actor      | Actions |
| :---        |    :---   |
| System | Tracks current inventory prices and sends updates to POSes if necessary |


## External System Adapters

All adapters consist of three optional components. Presence of each component depends on actual external system specs. As we don't have enough information availiable about actual systems we list all of them.

| Adapter      | Purpose
| :---        |    :---   |
| Price Updater | Notifies the external system to update price at a specific location for a specific item |
| Source Inventory Collector      | Gets udpates about inventory from the external system |
| Source Purchases Collector      | Gets udpates about purchases from the external system |

## External Survey System

Was chosen to be external because it is a large scope. It is more reasonable to integrate with 3rd party.

### Actions for Actors
| Actor      | Actions |
| :---        |    :---   |
| Customer | Submit answers to surveys |
| Kitchen Admin | Created surveys |


