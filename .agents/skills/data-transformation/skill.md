---
name: data-transformation
description: Process and format Free Fire API responses for different use cases including Discord bots, web dashboards, and calculating derived metrics
---

# Instructions

## Skill: Data Transformation & Formatting

This skill helps AI agents process and format API responses for different use cases.

### When to Use This Skill
- When building Discord bots with embeds
- When creating web dashboards
- When calculating derived metrics
- When formatting data for display
- When aggregating data from multiple endpoints

### Core Capabilities

AI agents should:
- Parse JSON responses correctly
- Extract relevant data fields
- Format data for display (Discord embeds, web dashboards, etc.)
- Calculate derived metrics (win rates, K/D ratios, etc.)

### Example: Format Player Stats

```python
def format_player_stats(stats_data):
    """Transform raw stats into readable format"""
    player_stats = stats_data['data']
    
    formatted = {
        'player_id': player_stats['uid'],
        'solo': {
            'win_rate': f"{(player_stats['solo']['wins'] / player_stats['solo']['gamesPlayed'] * 100):.1f}%",
            'kd_ratio': f"{player_stats['solo']['kd']:.2f}",
            'total_kills': player_stats['solo']['kills']
        },
        'duo': {
            'win_rate': f"{(player_stats['duo']['wins'] / player_stats['duo']['gamesPlayed'] * 100):.1f}%",
            'kd_ratio': f"{player_stats['duo']['kd']:.2f}",
            'total_kills': player_stats['duo']['kills']
        },
        'squad': {
            'win_rate': f"{(player_stats['squad']['wins'] / player_stats['squad']['gamesPlayed'] * 100):.1f}%",
            'kd_ratio': f"{player_stats['squad']['kd']:.2f}",
            'total_kills': player_stats['squad']['kills']
        }
    }
    
    return formatted
```

### Example: Discord Bot Embed

```python
import discord

def create_player_embed(player_data):
    """Create Discord embed from player data"""
    embed = discord.Embed(
        title=f"🎮 {player_data['name']}",
        description=f"Level {player_data['level']} | {player_data['region'].upper()}",
        color=0x00ff00
    )
    
    embed.add_field(name="UID", value=player_data['uid'], inline=True)
    embed.add_field(name="Rank", value=player_data['rank'], inline=True)
    embed.add_field(name="Clan", value=player_data.get('clan', 'None'), inline=True)
    
    if 'stats' in player_data:
        embed.add_field(
            name="📊 Stats",
            value=f"Wins: {player_data['stats']['wins']}\nKills: {player_data['stats']['kills']}",
            inline=False
        )
    
    return embed
```

### Common Derived Metrics

Calculate and format these metrics:
- **Win Rate:** `(wins / gamesPlayed) * 100`
- **K/D Ratio:** `kills / deaths`
- **Average Kills Per Game:** `kills / gamesPlayed`
- **Headshot Percentage:** `(headshots / kills) * 100`
- **Survival Rate:** `(survivals / gamesPlayed) * 100`
- **Top 3 Rate:** `(top3 / gamesPlayed) * 100`

### Best Practices
- Handle missing or null data gracefully
- Use appropriate decimal places for percentages (1-2)
- Format large numbers with commas or abbreviations
- Add appropriate emojis for visual appeal in chat bots
- Validate data before calculations (avoid division by zero)
- Use consistent formatting across all outputs
- Consider localization for international audiences
