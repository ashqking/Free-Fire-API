---
name: parameter-validation
description: Validate input parameters before making Free Fire API calls including UID format, region values, language codes, and map codes
---

# Instructions

## Skill: Parameter Validation

This skill helps AI agents validate input parameters before making API calls to the Free Fire API.

### When to Use This Skill
- Before making any API call
- When accepting user input
- When validating request parameters
- When building API client libraries

### Parameters to Validate

AI agents should validate:
- **UID Format:** 9-10 digit numeric string
- **Region Values:** Must be one of: `sg`, `ind`, `br`
- **Language Codes:** Valid options: `en`, `ar`, `es`, `id`, `pt`, `ru`, `vi`
- **Map Codes:** Alphanumeric, 8-12 characters for Craftland

### Example Validation Functions

```python
import re

def validate_uid(uid):
    """Validate Free Fire player UID"""
    if not re.match(r'^\d{9,10}$', str(uid)):
        raise ValueError("UID must be a 9-10 digit number")
    return str(uid)

def validate_region(region):
    """Validate game region"""
    valid_regions = ['sg', 'ind', 'br']
    if region not in valid_regions:
        raise ValueError(f"Region must be one of: {valid_regions}")
    return region

def validate_language(lang):
    """Validate language code"""
    valid_languages = ['en', 'ar', 'es', 'id', 'pt', 'ru', 'vi']
    if lang not in valid_languages:
        raise ValueError(f"Language must be one of: {valid_languages}")
    return lang

def validate_map_code(code):
    """Validate Craftland map code"""
    if not re.match(r'^[A-Za-z0-9]{8,12}$', code):
        raise ValueError("Map code must be 8-12 alphanumeric characters")
    return code
```

### Best Practices
- Validate all parameters before making API calls
- Provide clear, actionable error messages
- Return validated (sanitized) values
- Document accepted values in code comments
