## What is a UUID?

A **UUID (Universally Unique Identifier)** is a **128-bit value** used to uniquely identify things like:

- Database records  
- API requests  
- Users  
- Objects  

The goal is to make collisions so unlikely that, for practical purposes, they never happen.

---

## UUID Format

UUIDs are commonly represented as a **36-character string** made up of hexadecimal digits and hyphens:

```text
550e8400-e29b-41d4-a716-446655440000
```

## The Size of the UUID Number Space

Because a UUID is **128 bits**, there are `2^128 ≈ 3.4 × 10^38` possible values. That is about **340 undecillion** possible outcomes 

## Probability, Not Guarantees

UUIDs are not **mathematically guaranteed** to be unique. Instead, they are **probabilistically unique.**

Even at very large scales, the probability of generating the same UUID twice is **astronomically low**. This is why UUIDs work reliably in real-world systems, especially in **distributed environments** where coordination is expensive or impossible.

## UUID Versions

UUIDs come in multiple versions, each using a different strategy to ensure uniqueness:

- **UUID v1**: Time-based, generated using a timestamp and a node identifier  
- **UUID v4**: Randomly generated and the most commonly used version  
- **UUID v7**: Time-ordered with randomness, designed to improve database indexing and sorting  

Most modern systems use **UUID v4**, which relies on randomness rather than coordination, making it well-suited for distributed systems.