# Data Store Format

## Status
Accepted


## Context
System requires appropriate database technology which suites the needs around building a 360 view of a customer
Non-functional requirements around Availability, Flexibility to change also needs to be considered.

## Decision

We will use a graph database as a data store for Customer 360 application.

## Consequences

**Positive:**

- Fast multi-criteria search via relationship transversal
- Availability
- Flexibility to change
- Efficient recommendation algorithms

**Risks:**

- Likely requires training of current staff on this technology, or employment of staff already skilled

**Bonus Features:**

- Can model the database exactly how things are in the real world, with no joins or trying to fit data into a relational format