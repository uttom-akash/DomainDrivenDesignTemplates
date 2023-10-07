### Domain Driven Design Template

#### Layer description

##### API Layer

Provide the interface to outside world to communicate and contains.

- Controllers
- Handlers
- Consumers

##### Application Layer

Coordinate domain layers , infrastructure layers and external providers.
- Services
- coordination logics
- Dtos
- Ioc

##### Domain Layer

This is the heart of business logics and contains.

- Domain entity and related Business logics
- Repositories contracts

##### Infrastructure Layer

This provides the wrapper over the third party library and external providers. it contains
- wrapper over library
- Implementation of persistence storage

##### Background Task Layer

Offload the long running task and runs in background.
- Webjobs
- Azure Functions

##### Dependencies
```
API Layer               -> Application Layer

Application Layer       -> Domain Layer
Application Layer       -> Infrastructure Layer

Infrastructure Layer    -> Domain Layer

```


