---
name: multi-language-code-generation
description: Generate Free Fire API integration code examples in multiple programming languages including Python, JavaScript, PHP, cURL, Java, Go, and Ruby
---

# Instructions

## Skill: Multi-Language Code Generation

This skill helps AI agents generate code examples in multiple programming languages for Free Fire API integration.

### When to Use This Skill
- When users ask for code examples in specific languages
- When providing API integration tutorials
- When building SDK documentation
- When supporting diverse developer communities

### Supported Languages

AI agents should be able to generate equivalent implementations in:
- **Python** (with requests library)
- **JavaScript/Node.js** (with fetch or axios)
- **PHP** (with cURL)
- **cURL** (for command-line testing)
- **Java, Go, Ruby** (for enterprise applications)

### Example: Player Info Endpoint

#### Python
```python
import requests

headers = {'x-api-key': 'YOUR_API_KEY'}
params = {'region': 'ind', 'uid': '665951869'}

response = requests.get(
    'https://developers.freefirecommunity.com/api/v1/info',
    headers=headers,
    params=params
)

print(response.json())
```

#### JavaScript (Node.js with fetch)
```javascript
const response = await fetch(
  'https://developers.freefirecommunity.com/api/v1/info?region=ind&uid=665951869',
  {
    headers: {
      'x-api-key': 'YOUR_API_KEY'
    }
  }
);

const data = await response.json();
console.log(data);
```

#### PHP
```php
<?php
$ch = curl_init();
curl_setopt($ch, CURLOPT_URL, 'https://developers.freefirecommunity.com/api/v1/info?region=ind&uid=665951869');
curl_setopt($ch, CURLOPT_HTTPHEADER, [
  'x-api-key: YOUR_API_KEY'
]);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);

$response = curl_exec($ch);
echo $response;
?>
```

#### cURL
```bash
curl -X GET "https://developers.freefirecommunity.com/api/v1/info?region=ind&uid=665951869" \
  -H "x-api-key: YOUR_API_KEY"
```

### Code Generation Best Practices

When generating code:
1. **Use secure authentication** - Always use header-based authentication
2. **Include error handling** - Show proper error handling patterns
3. **Add comments** - Explain key concepts in code comments
4. **Use environment variables** - Never hardcode API keys
5. **Show complete examples** - Include imports and setup
6. **Follow language conventions** - Use idiomatic code for each language
7. **Include response handling** - Show how to parse JSON responses
8. **Add validation** - Include input parameter validation

### Language-Specific Considerations
- **Python:** Use `requests` library, handle exceptions
- **JavaScript:** Use `async/await`, handle promises
- **PHP:** Use cURL properly, handle errors
- **Java:** Use HttpClient, handle IOException
- **Go:** Use http.Client, handle errors explicitly
- **Ruby:** Use net/http or httparty gem
