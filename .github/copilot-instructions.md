# Copilot Instructions for NexusAI Workspace

## Architecture
- This is a Clean Architecture .NET solution: Domain / Application / Infrastructure / API
- API controllers delegate to Application layer services. Never put business logic in controllers.
- The Python service is FastAPI with Pydantic v2, SQLAlchemy 2.0 async, and dependency injection.
- React uses Vite + TypeScript + Tailwind CSS + Zustand.

## Patterns
- C#: Use Result<T> pattern for operations that can fail. Never throw exceptions for expected failures.
- C#: Use MediatR-style handlers in Application layer (or equivalent pattern).
- TypeScript: Use custom hooks for data fetching. Never fetch directly in components.
- Python: Use repository pattern with async SQLAlchemy. Never write raw SQL in endpoints.

## Security
- Validate all inputs with FluentValidation (C#) or Pydantic (Python).
- All API endpoints must check authorization. Use [Authorize] attributes.
- Never log secrets, tokens, or PII.

## Naming
- C#: PascalCase for classes/methods, camelCase for locals, _camelCase for private fields
- TypeScript: PascalCase for components/types, camelCase for functions/variables
- Python: snake_case for everything, PascalCase for Pydantic models
