---
name: software-architecture
description: Design and evaluate maintainable software architecture, boundaries, data flows and trade-offs in an existing product.
---

# Software Architecture

## Method
1. Understand business capabilities, users, critical workflows and quality attributes.
2. Map current architecture from source, not assumptions: modules, runtime, data stores, APIs, events and external services.
3. Identify coupling, ownership boundaries, trust boundaries and single points of failure.
4. Propose the smallest architecture that satisfies the requirements.
5. Compare viable options using maintainability, reliability, performance, security, delivery cost and migration risk.
6. Define contracts: interfaces, schemas, error behavior, ownership and compatibility.
7. Plan incremental migration with rollback and observability.
8. Document decisions in ADR format when a decision is durable.

## Do not
- Introduce microservices, abstractions or dependencies without a demonstrated need.
- Recommend replacing working infrastructure solely because a technology is fashionable.
- Ignore backward compatibility, data migration, offline behavior or platform constraints.

## Output
Context, constraints, options, recommendation, trade-offs, diagrams when useful, migration steps, risks and open decisions.
