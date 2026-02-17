---
description: REST API design principles and conventions
---

# API Design Rules

## RESTful Conventions
- Use proper HTTP methods (GET, POST, PUT, DELETE)
- Follow resource-based URL structure
- Use plural nouns for collections
- Implement proper status codes

## Endpoint Structure
```
/api/v1/auth/login
/api/v1/auth/register
/api/v1/users/profile
/api/v1/nightclubs/{id}/rooms
/api/v1/rooms/{id}/messages
/api/v1/reports
```

## Request/Response
- Use DTOs for all API communications
- Implement proper validation with @Valid
- Return consistent response format
- Use pagination for large datasets

## Authentication
- JWT-based authentication
- Bearer token in Authorization header
- Refresh token mechanism
- Role-based access control

## Error Handling
- Use @ControllerAdvice for global exception handling
- Return meaningful error messages
- Include error codes for client handling
- Log errors properly

## Security
- Validate all inputs
- Sanitize user data
- Implement rate limiting
- Use HTTPS everywhere

## Documentation
- Use OpenAPI/Swagger annotations
- Document all endpoints
- Include request/response examples
- Keep documentation updated
