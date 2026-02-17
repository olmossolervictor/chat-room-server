---
description: Spring Boot development best practices and conventions
---

# Spring Boot Development Rules

## Project Structure
- Follow standard Maven/Gradle structure
- Keep controllers thin, business logic in services
- Use DTOs for API requests/responses
- Separate concerns with proper layering

## Code Quality
- Use Lombok annotations to reduce boilerplate
- Implement proper exception handling with @ControllerAdvice
- Use @Valid for request validation
- Follow Java naming conventions

## Database
- Use JPA repositories for data access
- Implement proper entity relationships
- Use @Transactional for database operations
- Consider connection pooling configuration

## Security
- Implement JWT authentication for mobile API
- Use HTTPS in production
- Validate all inputs
- Implement rate limiting

## WebSocket Implementation
- Use @EnableWebSocket for real-time chat
- Implement proper session management
- Handle connection/disconnection events
- Consider message encryption

## Testing
- Write unit tests for services
- Use @SpringBootTest for integration tests
- Test WebSocket endpoints
- Mock external dependencies

## Performance
- Use caching where appropriate
- Optimize database queries
- Consider async processing for heavy operations
- Monitor application metrics
