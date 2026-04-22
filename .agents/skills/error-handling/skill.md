---
name: error-handling
description: Implement comprehensive error handling and retry logic for Free Fire API calls including rate limiting, network errors, and exponential backoff
---

# Instructions

## Skill: Error Handling & Retry Logic

This skill helps AI agents implement comprehensive error handling for Free Fire API integration.

### When to Use This Skill
- When making any API calls
- When building reliable applications
- When handling rate limits
- When implementing production-grade error recovery

### HTTP Status Codes to Handle

AI agents should handle:
- **400 Bad Request:** Invalid parameters
- **401 Unauthorized:** Invalid API key
- **404 Not Found:** Player or resource doesn't exist
- **429 Rate Limit:** Too many requests
- **500 Server Error:** API service issues

### Example Error Handling with Retry

```python
import time
from requests.exceptions import RequestException
import requests

def call_api_with_retry(url, headers, params, max_retries=3):
    """Call API with automatic retry logic"""
    for attempt in range(max_retries):
        try:
            response = requests.get(url, headers=headers, params=params)
            
            if response.status_code == 200:
                return response.json()
            elif response.status_code == 404:
                return {"error": "Player not found"}
            elif response.status_code == 429:
                # Rate limit - wait and retry
                wait_time = 60 * (attempt + 1)
                print(f"Rate limited. Waiting {wait_time}s...")
                time.sleep(wait_time)
                continue
            elif response.status_code == 401:
                raise Exception("Invalid API key")
            else:
                response.raise_for_status()
                
        except RequestException as e:
            if attempt == max_retries - 1:
                raise
            time.sleep(2 ** attempt)  # Exponential backoff
    
    return {"error": "Max retries exceeded"}
```

### Best Practices
- Implement exponential backoff for retries
- Respect rate limits (100 requests/hour on free tier)
- Log all errors for debugging
- Provide helpful error messages to end users
- Don't retry on 400/401 errors (client errors)
- Always set max retry limits
- Handle network timeouts gracefully
- Distinguish between client errors (4xx) and server errors (5xx)

### Rate Limit Strategy
- Free tier: 100 requests/hour
- If rate limited (429), wait 60 seconds before retry
- Implement request counting to stay within limits
- Consider caching to reduce API calls
