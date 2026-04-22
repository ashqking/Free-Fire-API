---
name: response-caching
description: Implement caching strategies to reduce Free Fire API calls and avoid rate limits with TTL-based cache management
---

# Instructions

## Skill: Response Caching

This skill helps AI agents implement caching to reduce API calls and avoid rate limits.

### When to Use This Skill
- When building applications that make frequent API calls
- When working with the free tier (100 requests/hour)
- When optimizing application performance
- When implementing rate limit management

### Caching Strategy

AI agents should:
- Cache player info responses (low change frequency)
- Use shorter TTL for dynamic data (stats, leaderboards)
- Implement cache invalidation strategies
- Respect rate limits (100 requests/hour on free tier)

### Example Caching Implementation

```python
from functools import lru_cache
import time

# Simple in-memory cache with TTL
cache = {}

def cached_api_call(cache_key, api_function, ttl_seconds=300):
    """Cache API responses with TTL"""
    current_time = time.time()
    
    if cache_key in cache:
        cached_data, timestamp = cache[cache_key]
        if current_time - timestamp < ttl_seconds:
            return cached_data
    
    # Make API call
    data = api_function()
    cache[cache_key] = (data, current_time)
    return data

# Usage example
def get_player_info_cached(region, uid):
    cache_key = f"player_info:{region}:{uid}"
    return cached_api_call(
        cache_key,
        lambda: get_player_info(region, uid),
        ttl_seconds=600  # 10 minutes
    )
```

### Recommended TTL Values
- **Player Profile Info:** 600-3600 seconds (10-60 minutes)
- **Player Stats:** 300-600 seconds (5-10 minutes)
- **Leaderboards:** 60-300 seconds (1-5 minutes)
- **Ban Status:** 300-600 seconds (5-10 minutes)
- **Static Assets:** 86400 seconds (24 hours)

### Best Practices
- Use in-memory caching for high-performance applications
- Consider Redis or Memcached for distributed applications
- Implement cache warming for frequently accessed data
- Set appropriate TTL based on data volatility
- Monitor cache hit rates
- Implement cache invalidation for critical updates
