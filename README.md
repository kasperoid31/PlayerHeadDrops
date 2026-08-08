<div align="center">

# 🎯 PlayerHeadDrops

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&pause=1200&color=F7A855&center=true&vCenter=true&width=640&height=46&lines=Every+kill+has+a+price.;Every+head+has+a+story." alt="motto" />

<br>

<img src="https://img.shields.io/badge/version-2.0.0-F7A855?style=for-the-badge&logo=semver&logoColor=white" alt="version">
<img src="https://img.shields.io/badge/Minecraft-1.13--26.2-4C9A2A?style=for-the-badge&logo=mojang&logoColor=white" alt="mc">
<img src="https://img.shields.io/badge/platform-Paper%20%7C%20Purpur%20%7C%20Spigot%20%7C%20Bukkit-9146FF?style=for-the-badge" alt="platform">
<img src="https://img.shields.io/badge/Java-8%2B-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="java">

</div>

---

## About the plugin

PlayerHeadDrops is a lightweight yet powerful plugin for all server cores that adds a realistic head drop system for both players and mobs. Every kill becomes meaningful with configurable chances, economy integration, and beautiful MiniMessage formatting.

---

## Features

| Feature | Description |
|---------|-------------|
| Player Heads | Configurable drop chance for player kills |
| Mob Heads | Support for zombies, skeletons, creepers, and more |
| MiniMessage | Beautiful gradient, bold, and HEX color messages |
| Economy | Vault integration for kill rewards |
| Anti-Farm | One-time drops and cooldown system |
| World Control | Whitelist/blacklist worlds |
| Effects | Sound and particle effects on drop |
| Custom Names | Fully customizable head names and lore |
| PlaceholderAPI | Dynamic placeholders in messages |

---

## Installation

1. Download the latest .jar from Modrinth or CurseForge
2. Place it in your server's plugins/ folder
3. Restart the server or use /reload
4. Configure config.yml and messages.yml
5. Done

---

## Commands

| Command | Description | Permission |
|---------|-------------|------------|
| /phd help | Show help menu | playerheaddrops.help |
| /phd reload | Reload config & messages | playerheaddrops.reload |
| /phd give <player> [receiver] | Give a player head | playerheaddrops.give |

---

## MiniMessage Examples

<details>
<summary>messages.yml (click to expand)</summary>

```yaml
prefix: "<gray>[</gray><gradient:#FFD700:#FF6B6B>PHD</gradient><gray>]</gray> "
announce: "<gradient:#ff0000:#ffff00>%player%</gradient> <gold>killed</gold> <gradient:#ff00ff:#00ffff>%killer%</gradient> <gray>and claimed their head!</gray>"
give-success: "<gradient:#00ff00:#00ff88>Head</gradient> <gradient:#ffd700:#ff6b00>%player%</gradient> <gradient:#00ff00:#00ff88>given to</gradient> <gradient:#4ECDC4:#44B39D>%receiver%</gradient>"
```

</details>

---

## Configuration

<details>
<summary>config.yml (click to expand)</summary>

```yaml
# Player head drop chance (0.0 - 1.0)
drop-chance: 0.5

# One-time drop per player
one-time-drop: false

# Cooldown in seconds
cooldown-seconds: 60

# Only PvP drops
only-pvp: false

# Mob heads
mob-heads:
  enabled: true
  default-chance: 0.05
  only-player-kill: true
  chances:
    ZOMBIE: 0.1
    SKELETON: 0.1
    CREEPER: 0.05

# Head customization
head:
  name-format: "%player%'s Head"
  name-color: "yellow"
  lore:
    - "&7Obtained: %date%"

# Economy rewards
economy:
  enabled: true
  reward: 10.0

# Announcements
announce:
  enabled: true
  message: "<yellow>%player%'s head has dropped!</yellow>"
  radius: 50

# Effects
effects:
  sound:
    enabled: true
    name: "entity.player.levelup"
  particles:
    enabled: true
    name: "SOUL"
```

</details>

---

## Permissions

| Permission | Description |
|------------|-------------|
| playerheaddrops.bypass | Bypass head drops entirely |
| playerheaddrops.boost | Double drop chance |
| playerheaddrops.give | Use /phd give |
| playerheaddrops.reload | Use /phd reload |

---

## Technical Details

| Technology | Version |
|------------|---------|
| Java | 8+ |
| Minecraft | 1.13 - 26.2 |
| Platform | Paper, Purpur |
| MiniMessage | Supported |
| PlaceholderAPI | Ready |
| Vault | Integrated |

---

## Compatibility

| Platform | Versions | Status |
|----------|----------|--------|
| Paper | 1.13 - 26.2 | Fully supported |
| Purpur | 1.13 - 26.2 | Fully supported |
| Spigot | 1.13 - 1.21 | Limited support |
| Bukkit | 1.13 - 1.21 | Limited support |

---

## Links

- [Modrinth](https://modrinth.com/plugin/playerheaddrops)
- [CurseForge](https://www.curseforge.com/minecraft/bukkit-plugins/playerheaddrops)
- [GitHub](https://github.com/kasperoid31)
- [Telegram News](https://t.me/prostoimpery)
- [Telegram Channel](https://t.me/pro100chnl)
- [Author Profile](https://modrinth.com/user/kasperoid)

---

## FAQ

<details>
<summary>Does this work with 1.13?</summary>
Yes, the plugin is compatible with Paper and Purpur versions 1.13 through 26.2.
</details>

<details>
<summary>Can I use this with Spigot?</summary>
Yes, but MiniMessage features may have limited functionality on older Spigot builds. Paper or Purpur is recommended for full experience.
</details>

<details>
<summary>Does it support PlaceholderAPI?</summary>
Yes, every message supports PlaceholderAPI placeholders.
</details>

<details>
<summary>What Java version is required?</summary>
Java 8 or higher.
</details>

---

## Author

[Kasperoid](https://modrinth.com/user/kasperoid)

---

## License

All Rights Reserved (ARR)

This plugin is closed-source software. Copying, modifying, distributing, or using without explicit permission from the author is prohibited.

For inquiries or collaboration requests, contact the author directly.

---

<div align="center">

### PlayerHeadDrops
Every kill has a price. Every head has a story.

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:000000,55:F7A855,100:000000&height=130&section=footer" alt="" width="100%" />

</div>
