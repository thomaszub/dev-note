# Entity-Component-System architecture

The Entity-Component-System architecture is mainly used in game development to overcome the design problem of a domain with many entities with different but shared characteristics, named components, which can possibly change during runtime. 
In a naive design this would lead to a deep and complex inheritence structure or many different classes injecting the necessary components with a mechanism to handle the removal or addition of components.

The Entity-Component-System architecture is mainly data-driven and can be seen as the implementation of an in-memory database.

## Entity

The entity is an object of the domain, which can be recognised by a unique identifier. Typically the unique identifier is the only member of an entity class.

## Component

A component represents a functional aspect of the domain, one or multiple instances of a component represent this aspect for a specific entity. The instances are connected with the entity by the unique identifier of the entity.

## System

The system executes business logic on every entity using the needed components of the entity according to the executed command.
