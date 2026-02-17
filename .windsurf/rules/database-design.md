---
description: PostgreSQL database design rules and patterns
---

# Database Design Rules

## Entity Design
- Use @Entity annotations with proper table names
- Define @Id with @GeneratedValue strategy
- Use @Column annotations for constraints
- Implement proper relationships (@OneToMany, @ManyToOne, etc.)

## Indexing Strategy
- Add indexes on foreign keys
- Index frequently queried columns
- Consider composite indexes for complex queries
- Monitor query performance

## Data Types
- Use appropriate data types for efficiency
- TEXT for long messages
- TIMESTAMP for temporal data
- UUID for unique identifiers
- BOOLEAN for flags

## Constraints
- Define NOT NULL constraints
- Use UNIQUE constraints where needed
- Implement CHECK constraints for data validation
- Set proper CASCADE rules for relationships

## Performance
- Use connection pooling (HikariCP)
- Configure proper batch sizes
- Consider read replicas for scaling
- Monitor slow queries

## Migration Strategy
- Use Flyway or Liquibase for schema changes
- Version control all migrations
- Test migrations on staging
- Plan rollback strategies
