# Dapper over Entity Framework Core

Dapper was chosen over EF Core for database access. The schema is simple, and writing real SQL is a more transferable backend skill than learning EF Core's abstraction layer — the goal is to understand exactly what is hitting the database, not to hide it behind a query builder. DbUp is used for migrations in place of EF Core's migration tooling; migrations are plain `.sql` files consistent with the same philosophy.

## Considered Options

- EF Core — rejected in favour of learning fundamentals; can be revisited if schema complexity grows substantially
