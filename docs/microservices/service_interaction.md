# Service interaction

This note describes interaction procedures used in microservice architectures.

## Choreography

In the choreography each service knows its role in a business process and therefore it needs to know all following services it has to call for the business process.

```mermaid
sequenceDiagram
  participant Service1
  participant Service2
  participant Service3
  Service1->>Service2: request
  Service1->>Service3: request
  Service3->>Service2: request
```
__Note__: Response side suppressed for clarity.

## Orchestration

In the orchestration a business process is executed by a central coordinator. The services theirself do not have to know the underlying business process and services involved in the business process.

```mermaid
sequenceDiagram
  participant Coordinator
  participant Service1
  participant Service2
  participant Service3
  Coordinator->>Service1: request
  Coordinator->>Service2: request
  Coordinator->>Service3: request
  Coordinator->>Service2: request
```
__Note__: Response side suppressed for clarity.

## Another definition

Choreography = Event-driven communication

Orchestration = Command-driven communication