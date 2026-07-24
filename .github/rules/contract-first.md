# Contract-First Rule

When frontend and backend both change, contract approval is mandatory before implementation.

## Contract Candidates

- OpenAPI/Swagger
- GraphQL schema
- gRPC proto
- AsyncAPI
- JSON Schema
- Shared TypeScript interfaces
- Event contracts

## Required Contract Content

- endpoints or operations
- request and response models
- validation rules
- authentication and authorization
- error responses and status codes
- pagination, sorting, filtering
- versioning
- file formats when applicable

## Synchronization Requirements

1. Freeze approved contract.
2. Store contract in shared memory.
3. Generate shared types where possible.
4. Keep frontend and backend aligned to the same contract version.
5. On contract change, update memory, regenerate types, update tests, and notify participating agents.
