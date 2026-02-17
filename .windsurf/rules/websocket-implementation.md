---
description: WebSocket implementation rules for real-time chat
---

# WebSocket Implementation Rules

## Configuration
- Use @EnableWebSocket annotation
- Implement WebSocketConfigurer
- Configure proper message handlers
- Set up session management

## Message Handling
- Use @MessageMapping for endpoints
- Implement @SubscribeMapping for subscriptions
- Handle different message types (chat, system, etc.)
- Validate incoming messages

## Session Management
- Track user sessions properly
- Handle connection/disconnection events
- Implement session cleanup on logout
- Store session metadata (location, room, etc.)

## Security
- Authenticate WebSocket connections
- Validate user permissions per room
- Implement rate limiting for messages
- Filter sensitive information

## Performance
- Use message brokers (RabbitMQ/Kafka) for scaling
- Implement proper error handling
- Monitor connection health
- Handle reconnection logic

## Message Format
```json
{
  "type": "CHAT_MESSAGE",
  "roomId": "uuid",
  "userId": "uuid", 
  "content": "encrypted_message",
  "timestamp": "ISO8601"
}
```

## Error Handling
- Handle connection failures gracefully
- Implement retry mechanisms
- Log connection issues
- Provide user feedback
