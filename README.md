# 🔥 Free Fire Information API

[![API Version](https://img.shields.io/badge/API-v2.0-blue.svg)](https://api.freefirecommunity.com)
[![Status](https://img.shields.io/badge/Status-Online-success.svg)](https://api.freefirecommunity.com/api/status)
[![License](https://img.shields.io/badge/License-Commercial-orange.svg)](https://api.freefirecommunity.com/terms)
[![Telegram](https://img.shields.io/badge/Support-@ashqking-blue.svg)](https://t.me/ashqking)

> **The most comprehensive and reliable FreeFire Player Information API** with advanced image aggregation, multi-source reliability, and enterprise-grade performance.

## 🚀 What Makes This API Special?

- **🎯 Real-Time Player Data** - Get live player statistics, ranks, and profile information
- **🖼️ Smart Image Aggregation** - Multi-source image fetching with automatic fallbacks
- **🌍 Global Coverage** - Supports all FreeFire regions (IND, BR, SG, US, VN, TH, ID, etc.)
- **⚡ Lightning Fast** - Optimized caching and CDN delivery
- **�️ Enterprise Security** - Rate limiting, API key management, and secure endpoints
- **📊 Comprehensive Data** - Player stats, clan info, pet details, weapon skins, and more

## 📊 Live API Response Example

```json
{
  "success": true,
  "api_info": {
    "remaining_requests": 499,
    "reset_date": "2025-09-01T20:57:13.154387"
  },
  "data": {
    "basicInfo": {
      "accountId": "665951869",
      "nickname": "FFC•ASHQKING",
      "level": 61,
      "rank": 306,
      "rankingPoints": 1530,
      "region": "IND",
      "liked": 4221,
      "badgeId": 1001000087,
      "bannerId": 901000159,
      "headPic": 902000226,
      "weaponSkinShows": [907193003, 912000005]
    },
    "clanBasicInfo": {
      "clanName": "ƝEOƝ»Ᏻᴀɴɢ×͜×",
      "clanLevel": 3,
      "memberNum": 34,
      "capacity": 40
    },
    "petInfo": {
      "id": 1300000111,
      "level": 5,
      "skinId": 1310000111,
      "selectedSkillId": 1315000009
    },
    "profileInfo": {
      "avatarId": 102000004,
      "equipedSkills": [203000629, 211000167, 205033049]
    }
  }
}
```

## 🎯 Key Features

### 📈 Player Information API
- **Complete Player Profiles** - Name, level, rank, statistics
- **Battle Royale Rankings** - Current rank, points, max rank achieved
- **Clash Squad Data** - CS rank, points, match history
- **Account Analytics** - Creation date, last login, experience points
- **Social Stats** - Likes, signature, language preferences

### 🖼️ Advanced Image System
- **Multi-Source Aggregation** - Fetches from 3+ reliable sources
- **Automatic Fallbacks** - 99.9% image availability
- **Direct Image URLs** - Clean, fast, cacheable image endpoints
- **High-Quality Assets** - Avatars, banners, badges, weapon skins

### 🏆 Clan & Team Data
- **Clan Information** - Name, level, member count, captain details
- **Team Statistics** - Member rankings, clan achievements
- **Leadership Data** - Captain profiles and clan management info

### 🐾 Pet & Equipment
- **Pet Statistics** - Level, skills, experience, skins
- **Weapon Loadouts** - Equipped skins, weapon preferences
- **Skill Configurations** - Active skills and character builds

## 🌟 API Endpoints

### 🔍 Player Information
```http
GET /api/player-info?uid={PLAYER_UID}&region={REGION}&api_key={YOUR_KEY}
```

**Supported Regions:** `IND`, `BR`, `SG`, `US`, `VN`, `TH`, `ID`, `MY`, `PH`, `PK`, `BD`, `RU`, `CIS`, `ME`, `TW`

### 🖼️ Player Images & Assets
```http
GET /api/images/player-assets?uid={PLAYER_UID}&region={REGION}&api_key={YOUR_KEY}
```

**Returns:** Avatar, banner, badge, weapon skins, pet skins with direct image URLs

### 🎨 Individual Item Images
```http
GET /api/images/item?item_id={ITEM_ID}&api_key={YOUR_KEY}
```

**Direct Image Access:**
```http
GET /api/images/item/{ITEM_ID}
```

### 📊 Usage Statistics
```http
GET /api/usage?api_key={YOUR_KEY}
```

### 🔧 System Health
```http
GET /api/images/sources-status?api_key={YOUR_KEY}
```

## 🚀 Quick Start

### 1️⃣ Get Your API Key
📱 **Contact:** [@ashqking on Telegram](https://t.me/ashqking)
- ⚡ **Instant Setup** - Get your key in minutes
- 💎 **Free Tier Available** - 500 requests/month
- 🚀 **Pro Plans** - Up to 50K requests/month
- 🏢 **Enterprise** - Unlimited requests + priority support

### 2️⃣ Make Your First Request

#### JavaScript/Node.js
#### JavaScript/Node.js
```javascript
const response = await fetch('https://api.freefirecommunity.com/api/player-info?uid=665951869&region=IND&api_key=YOUR_KEY');
const playerData = await response.json();
console.log(`Player: ${playerData.data.basicInfo.nickname} (Level ${playerData.data.basicInfo.level})`);
```

#### Python
```python
import requests

response = requests.get('https://api.freefirecommunity.com/api/player-info', {
    'uid': '665951869',
    'region': 'IND', 
    'api_key': 'YOUR_KEY'
})
player_data = response.json()
print(f"Player: {player_data['data']['basicInfo']['nickname']}")
```

#### cURL
```bash
curl "https://api.freefirecommunity.com/api/player-info?uid=665951869&region=IND&api_key=YOUR_KEY"
```

### 3️⃣ Get Player Images
```javascript
// Get all player images
const images = await fetch('https://api.freefirecommunity.com/api/images/player-assets?uid=665951869&region=IND&api_key=YOUR_KEY');
const imageData = await images.json();

// Direct image access
const avatarUrl = `https://api.freefirecommunity.com/api/images/item/${imageData.data.avatar.id}`;
```

## 🌍 Use Cases

### 🎮 Gaming Applications
- **Player Profile Viewers** - Display comprehensive player statistics
- **Clan Management Tools** - Track member progress and rankings
- **Tournament Platforms** - Verify player credentials and stats
- **Leaderboards** - Real-time ranking displays

### 📱 Mobile Apps
- **FreeFire Companions** - Enhanced player experience apps
- **Stat Tracking** - Progress monitoring and analytics
- **Social Features** - Player discovery and networking
- **Asset Galleries** - Showcase weapon skins and items

### 🌐 Web Platforms
- **Gaming Communities** - Player profiles and clan pages
- **Esports Websites** - Tournament management and statistics
- **Content Creation** - Data-driven content and analytics
- **Fan Sites** - Comprehensive FreeFire databases

## 📚 Integration Examples

### React/Next.js Component
```jsx
import { useState, useEffect } from 'react';

function PlayerProfile({ uid, region }) {
  const [player, setPlayer] = useState(null);
  
  useEffect(() => {
    fetch(`https://api.freefirecommunity.com/api/player-info?uid=${uid}&region=${region}&api_key=${API_KEY}`)
      .then(res => res.json())
      .then(data => setPlayer(data.data));
  }, [uid, region]);

  if (!player) return <div>Loading...</div>;

  return (
    <div className="player-card">
      <img src={`https://api.freefirecommunity.com/api/images/item/${player.profileInfo.avatarId}`} alt="Avatar" />
      <h2>{player.basicInfo.nickname}</h2>
      <p>Level: {player.basicInfo.level}</p>
      <p>Rank: {player.basicInfo.rank}</p>
      <p>Clan: {player.clanBasicInfo?.clanName}</p>
    </div>
  );
}
```

### Vue.js Integration
```vue
<template>
  <div class="player-dashboard">
    <player-card :player="playerData" />
    <clan-info :clan="playerData?.clanBasicInfo" />
  </div>
</template>

<script>
export default {
  data() {
    return { playerData: null };
  },
  async mounted() {
    const response = await fetch(`https://api.freefirecommunity.com/api/player-info?uid=${this.uid}&region=${this.region}&api_key=${this.apiKey}`);
    this.playerData = (await response.json()).data;
  }
};
</script>
```

## �️ Advanced Usage

### Rate Limiting & Error Handling
```javascript
class FreeFIreAPI {
  constructor(apiKey) {
    this.apiKey = apiKey;
    this.baseURL = 'https://api.freefirecommunity.com';
  }

  async makeRequest(endpoint, params = {}) {
    try {
      const url = new URL(`${this.baseURL}${endpoint}`);
      url.searchParams.append('api_key', this.apiKey);
      
      Object.entries(params).forEach(([key, value]) => {
        url.searchParams.append(key, value);
      });

      const response = await fetch(url);
      
      if (response.status === 429) {
        throw new Error('Rate limit exceeded. Please wait before making more requests.');
      }
      
      return await response.json();
    } catch (error) {
      console.error('API Request failed:', error);
      throw error;
    }
  }

  async getPlayer(uid, region) {
    return this.makeRequest('/api/player-info', { uid, region });
  }
  
  async getPlayerImages(uid, region) {
    return this.makeRequest('/api/images/player-assets', { uid, region });
  }
}
```

### Caching Strategy
```javascript
class CachedFreeFIreAPI extends FreeFIreAPI {
  constructor(apiKey, cacheExpiry = 300000) { // 5 minutes default
    super(apiKey);
    this.cache = new Map();
    this.cacheExpiry = cacheExpiry;
  }

  async makeRequest(endpoint, params = {}) {
    const cacheKey = `${endpoint}:${JSON.stringify(params)}`;
    const cached = this.cache.get(cacheKey);
    
    if (cached && Date.now() - cached.timestamp < this.cacheExpiry) {
      return cached.data;
    }

    const data = await super.makeRequest(endpoint, params);
    this.cache.set(cacheKey, { data, timestamp: Date.now() });
    
    return data;
  }
}
```

## 📊 Response Schema

### Player Information Response
```typescript
interface PlayerResponse {
  success: boolean;
  api_info: {
    remaining_requests: number;
    reset_date: string;
  };
  data: {
    basicInfo: {
      accountId: string;
      nickname: string;
      level: number;
      rank: number;
      rankingPoints: number;
      region: string;
      liked: number;
      badgeId: number;
      bannerId: number;
      headPic: number;
      weaponSkinShows: number[];
    };
    clanBasicInfo?: {
      clanName: string;
      clanLevel: number;
      memberNum: number;
      capacity: number;
    };
    petInfo: {
      id: number;
      level: number;
      skinId: number;
      selectedSkillId: number;
    };
    profileInfo: {
      avatarId: number;
      equipedSkills: number[];
    };
  };
}
```

## 🔧 Status Codes & Error Handling

| Code | Status | Description |
|------|--------|-------------|
| `200` | ✅ Success | Request successful |
| `400` | ❌ Bad Request | Missing or invalid parameters |
| `401` | 🔒 Unauthorized | Invalid or missing API key |
| `429` | ⏱️ Rate Limited | Too many requests |
| `404` | 🚫 Not Found | Player or resource not found |
| `500` | ⚠️ Server Error | Internal server error |

## 📞 Support & Community

- **📱 Primary Support:** [@ashqking on Telegram](https://t.me/ashqking)
- **📧 Business Inquiries:** enterprise@freefirecommunity.com
- **📚 Documentation:** [https://api.freefirecommunity.com/docs](https://api.freefirecommunity.com/docs)
- **🆘 Issues:** Create an issue in this repository
- **💬 Community:** Join our Telegram group for developers

## ⚖️ Legal & Compliance

- **🔒 Privacy:** We respect user privacy and GDPR compliance
- **� Terms:** See [Terms of Service](https://api.freefirecommunity.com/terms)
- **⚠️ Disclaimer:** This is an unofficial third-party API service
- **🚫 Not Affiliated:** Not affiliated with Garena or FreeFire
- **📜 Commercial Use:** Commercial licensing available

## 🚀 Roadmap

- **🔄 Real-time Updates** - WebSocket support for live data
- **📊 Advanced Analytics** - Player progression tracking
- **🎮 Match History** - Detailed game statistics
- **🏆 Tournament API** - Esports integration features
- **🤖 AI Insights** - Player performance analytics
- **📱 Mobile SDK** - Native mobile integrations

## 📈 Performance Metrics

- **⚡ Response Time:** < 200ms average
- **🔄 Uptime:** 99.9% SLA guarantee
- **🌍 Global CDN:** Optimized worldwide delivery
- **📊 Cache Hit Rate:** 95%+ for popular queries
- **🔒 Security:** Enterprise-grade protection

---

<div align="center">

**Ready to supercharge your FreeFire application?**

[![Get API Key](https://img.shields.io/badge/Get%20API%20Key-@ashqking-blue.svg?style=for-the-badge)](https://t.me/ashqking)
[![Documentation](https://img.shields.io/badge/View%20Docs-API%20Guide-green.svg?style=for-the-badge)](https://api.freefirecommunity.com/docs)
[![Live Demo](https://img.shields.io/badge/Live%20Demo-Try%20Now-orange.svg?style=for-the-badge)](https://api.freefirecommunity.com)

</div>

---

<div align="center">
  <sub>Built with ❤️ for the FreeFire community | Powered by advanced multi-source technology</sub>
</div>
