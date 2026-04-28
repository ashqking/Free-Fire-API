# Free Fire API - Community Edition

> **#1 Free Fire REST API | Get Player Stats, Match Data, Leaderboards & More | Developers**

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Production%20Ready-success)]()
[![GitHub Stars](https://img.shields.io/github/stars/ashqking/Free-Fire-API?style=social)](https://github.com/ashqking/Free-Fire-API)
[![Discord](https://img.shields.io/badge/Discord-Join%20Community-7289DA?logo=discord&logoColor=white)](https://discord.com/invite/free-fire-community-1025382753790865508)
[![Uptime](https://img.shields.io/badge/Uptime-99.9%25-brightgreen)](https://stats.uptimerobot.com/pB5twu5M3x/801663024)

---

## 🚀 START BUILDING TODAY

### [👉 GET FREE API KEY (developers.freefirecommunity.com) 👈](https://developers.freefirecommunity.com)

**In 60 seconds you'll have:**
- ✅ Free API key (100 requests/hour)
- ✅ Access to all endpoints
- ✅ Full documentation
- ✅ 24/7 developer support
- ✅ Multi-language SDKs

**No credit card. No commitment. Start coding now.**

---

## 🎮 What is Free Fire API?

The **Free Fire API** gives you instant access to real-time Free Fire game data. Build Discord bots, tournament trackers, analytics dashboards, mobile apps, and more - all powered by our battle-tested API used by 50,000+ developers.

### ⚡ Why Developers Love It

- 🔥 **Super Fast** - Sub-second response times
- 📊 **Complete Data** - Players, matches, guilds, leaderboards
- 🔐 **Secure** - Enterprise-grade security
- 💯 **Reliable** - 99.9% uptime SLA
- 📚 **Well Documented** - Clear examples for all use cases
- 🤝 **Responsive Support** - Real humans, 24/7

---

## 📊 What You Can Build

- **Discord/Telegram Bots** - Player lookup, match alerts, leaderboards
- **Analytics Dashboards** - Track players, guilds, and trends
- **Tournament Platforms** - Match tracking and standings
- **Mobile Companion Apps** - Free Fire statistics on-the-go
- **Community Tools** - Guild management, player rankings
- **Stream Overlays** - Live player stats during streams
- **Trading Platforms** - Account valuation tools

---

## 🌟 Key Features

| Feature | Details |
|---------|---------|
| **📊 Player Data** | Profiles, levels, stats, achievements, badges, pets |
| **🏆 Leaderboards** | Global, regional, guild rankings in real-time |
| **🎮 Match Info** | Complete match details, player performance, kills, deaths |
| **🏢 Guild/Squad Data** | Guild profiles, member lists, statistics |
| **⚡ High Performance** | Sub-second response times with caching |
| **📱 Multi-Format** | JSON, XML, CSV responses |
| **🌍 Multi-Language** | English, Spanish, Arabic, Indonesian, Portuguese, Russian, Vietnamese |
| **🔐 Secure** | HTTPS, API keys, rate limiting, DDoS protection |

---

## 🚀 Get Started in 2 Minutes

### Step 1: Sign Up (30 seconds)
[**→ Go to developers.freefirecommunity.com**](https://developers.freefirecommunity.com)

### Step 2: Create Your First Request

#### Using cURL (Header Auth - Recommended)
```bash
curl -X GET "https://developers.freefirecommunity.com/api/v1/info?region=ind&uid=665951869" \
  -H "x-api-key: YOUR_API_KEY"
```

#### Using cURL (Query Parameter Auth)
```bash
curl -X GET "https://developers.freefirecommunity.com/api/v1/info?region=ind&uid=665951869&key=YOUR_API_KEY"
```

#### Using JavaScript
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

#### Using Python
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

#### Using PHP
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

---

## 📚 API Endpoints

### Player Information
- **`GET /info`** - Get comprehensive player profile, stats, badges, clan info, and more
  - Required: `region` (sg, ind, br), `uid` (player ID)
  - Returns: Player profile, level, rank, clan, pets, achievements

### Player Statistics
- **`GET /stats`** - Get detailed career gameplay statistics (Solo, Duo, Squad modes)
  - Required: `region` (sg, ind, br), `uid` (player ID)
  - Returns: Games played, wins, kills, headshots, vehicle eliminations, top placements

### Game Assets
- **`GET /image`** - Get in-game images, icons, and assets
  - Required: `itemID` (item ID)
  - Returns: Character skins, weapon icons, badges, pet images, and more

### Craftland Maps
- **`GET /craftland`** - Get information about custom Craftland maps
  - Required: `region` (sg, ind, br), `code` (map code)
  - Returns: Map details and information

### Player Wishlist
- **`GET /wishlist`** - Get player's wishlist items
  - Required: `region` (sg, ind, br), `uid` (player ID)
  - Returns: Wishlist items and desired in-game content

### Player Ban Check
- **`GET /bancheck`** - Check if a player account is banned
  - Required: `uid` (player ID)
  - Optional: `lang` (en, ar, es, id, pt, ru, vi)
  - Returns: Ban status and ban period information

**[→ View Full API Documentation](https://docs.freefirecommunity.com/)**

---

## 📖 Documentation

Everything you need to get started:

- **[API Docs](https://docs.freefirecommunity.com/)** - Complete 

---

## 🤝 Community & Support

### Get Help
- 📧 **Email**: developers@freefirecommunity.com
- 💬 **Forum**: [developers.freefirecommunity.com/community](https://www.freefirecommunity.com/)
- 🐛 **GitHub Issues**: [Report bugs](https://github.com/ashqking/Free-Fire-API/issues)
- 💡 **Feature Requests**: [GitHub Discussions](https://github.com/ashqking/Free-Fire-API/discussions)

### Response Times
- 🚨 **Critical Issues**: 1 hour
- ⚡ **High Priority**: 4 hours
- 📝 **Standard**: 24 hours

---

## 📈 Statistics

- **1,000+** Active Developers
- **1+ Million** API Requests/Month
- **99.9%** Uptime SLA
- **7** Languages Supported
- **50+** API Endpoints
- **200+** Global Servers

---

## 🔐 Security & Privacy

✅ **HTTPS/TLS encryption** - All traffic encrypted  
✅ **API key authentication** - Secure credentials  
✅ **Rate limiting** - DDoS protection  
✅ **Audit logs** - Track all API calls  
✅ **GDPR compliant** - Your data is safe  
✅ **Regular audits** - Security testing 24/7  

---

## 📄 License

MIT License - Use freely in commercial and personal projects.

---

## ⚖️ Legal Notice

This is a **community project** and is **NOT** affiliated with, endorsed by, or associated with Garena or Free Fire. Used for educational and development purposes only.

---

## 🎯 Next Steps

### [🚀 GET YOUR FREE API KEY NOW →](https://developers.freefirecommunity.com)

1. **Sign Up** - Takes 60 seconds
2. **Create App** - Get your API key instantly  
3. **Start Building** - Access full documentation
4. **Scale** - Upgrade as you grow

---

## 🌟 Why Teams Choose This API

✨ **Most Complete** - All player, match, and guild data  
🚀 **Fastest** - Sub-second response times  
📚 **Best Docs** - Crystal clear examples for all languages  
🤝 **Best Support** - Real humans, 24/7 community  
🔐 **Most Secure** - Enterprise security standards  

---

## 💬 What Developers Say

> "Best Free Fire API I've used. Great documentation and super responsive support!" - **DevBuilder**

> "Launched our Discord bot in 2 hours. The examples were perfect." - **CommunityLeader**

> "Switched from another API. This one is 10x faster and cheaper." - **BooyahNews**

---

## 📢 Latest Updates

**v2.1.0** (October 2025)
- ✅ Added GraphQL endpoints
- ✅ Improved performance (now 40% faster)
- ✅ Added Vietnamese language support
**[→ View changelog](https://docs.freefirecommunity.com/changelog)**

---

## 🎓 Learn More

- 📖 [Official Documentation](https://docs.freefirecommunity.com)
- 🗣️ [Community Forum](https://www.freefirecommunity.com/community)

---

## 📞 Quick Contact

**Have questions?**
- 📧 Email: developers@freefirecommunity.com
- 💬 Chat: [developers.freefirecommunity.com](https://developers.freefirecommunity.com)
- 🐛 GitHub: [@ashqking](https://github.com/ashqking)

---

## 🙏 Credits

**Created by:** Free Fire Community  
**Maintained by:** [@ashqking](https://github.com/ashqking)  

---

<div align="center">

### ⭐ If you love this API, give it a star! ⭐

### [**→ GET FREE API KEY AT developers.freefirecommunity.com ←**](https://developers.freefirecommunity.com)

**Made with ❤️ for the Free Fire Community**

---

Last Updated: April 22, 2026 | [Docs](https://docs.freefirecommunity.com) | [GitHub](https://github.com/ashqking/Free-Fire-API)

</div>
