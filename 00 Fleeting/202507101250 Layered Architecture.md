# Layered Architecture Style (n-tiered)

## Overview

- Components are organized into **logical horizontal layers**, each responsible for a specific technical concern
- This is **technically partitioned architecture**, meaning components area separated based on their **technical role** (e.g., UI, business logic, data access), rather than by domain logic
- Promotes separation of concerns, making the system easier to manage and understand

[[202507101250 Layered Architecture.excalidraw]]

## Typical Layers

Although there's no strict rule, mostly layered architecture use the following four layers:

1. Presentation

- Handles UI and user interactions
- Send user input to the business layer

2. Business

- Contains core application logic and rules
- Coordinates activities between the presentation and persistence layers

3. Persistence

- Manages data access logic
- Interfaces with the database

4. Database

- The actual data store (e.g., SQL, NoSQL database)

## Deployment Variants

- All-in-one (monolith): All layers deployed together (common in small apps or in-memory DB)
- Split into front-end, back-end, and database:
  - Presentation as the frontend
  - Business and persistence as the backend
  - Database as a separate external service

## Layer Isolation

- Layers isolation means that each layer can be modified independently of others
- In a closed layer model, requests must pass through each layer sequentially-no skipping is allowed (e.g., the presentation layer cannot talk directly  to the database)

## Strengths

- Simplicity: Easy to understand and implement
- Cost-effective: Low development and maintenance cost
- Good for small to medium applications or system with well-defined roles

## Risks / Weaknesses

- Tight coupling between layers: A failure in one layer (e.g., database) can cause the whole application to fail
- High mean time to recover (MTTR): Recovery from failure might take longer
- May not scale well not highly distributed or performance-intensive systems
