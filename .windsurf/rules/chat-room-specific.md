---
description: Chat room application specific rules and requirements
---

# Chat Room Application Rules

## Core Features Implementation
- QR code scanning integration with nightclub IDs
- User authentication and session management
- Location-based access control
- Room management (2-4 people per room)
- Real-time messaging with WebSocket
- Message encryption and privacy
- Auto-delete on location exit
- Report and security features

## Entity Relationships
- User → Nightclub (many-to-many via location)
- User → Room (many-to-many)
- Room → Messages (one-to-many)
- Nightclub → Rooms (one-to-many)
- User → Reports (one-to-many)

## Security Requirements
- End-to-end message encryption
- User location validation
- Report system for harassment
- Secure session management
- GDPR compliance for data deletion

## API Design
- RESTful endpoints for CRUD operations
- WebSocket for real-time messaging
- Location-based filtering
- Rate limiting per user
- Input validation and sanitization

## Database Design
- Optimize for concurrent access
- Implement proper indexing
- Consider data retention policies
- Backup and recovery strategies

## Mobile Integration
- JWT-based authentication
- Location services integration
- Push notifications for new messages
- Offline message queuing
- Background location tracking
