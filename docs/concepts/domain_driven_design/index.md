# Domain-driven design

This note contains informations about domain-driven design.

## Bounded context

The bounded context is the context in which a model applies. It explicitly set boundaries to other bounded contexts.

### Example: Customer

An example of different bounded contexts with a customer model is:

* Marketing -> Social interest, likes, needs
* Invoice -> Address, payment method
* Support -> Tickets

All these three bounded contexts share the customer as a boundary.