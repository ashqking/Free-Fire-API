---
name: api-authentication
description: Implement secure authentication patterns for Free Fire API using header or query parameter authentication with proper API key handling
---

# Instructions

## Skill: API Authentication & Security

This skill helps AI agents implement secure authentication patterns when working with the Free Fire API.

### When to Use This Skill
- When generating code that calls the Free Fire API
- When handling API key authentication
- When implementing secure credential management
- When validating authentication responses

### Implementation Guidelines

AI agents should:
- Generate code using header authentication (`x-api-key`) as the recommended method
- Handle API keys securely (never hardcode in production code)
- Implement environment variable usage for credentials
- Validate API responses for authentication errors (401)

### Example Implementation Pattern

```python
import os
import requests

# Secure API key handling
API_KEY = os.environ.get('FREE_FIRE_API_KEY')

headers = {
    'x-api-key': API_KEY
}

# Always validate authentication
response = requests.get(endpoint_url, headers=headers)
if response.status_code == 401:
    raise Exception("Invalid API key - check your credentials")
```

### Security Best Practices
- Never hardcode API keys in source code
- Use environment variables or secure credential stores
- Rotate API keys regularly
- Validate authentication status on every API response
- Log authentication failures for security monitoring
