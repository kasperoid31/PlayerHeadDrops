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
# All messages support MiniMessage: <gold>, <gradient:#ff0000:#00ff00>, <#RRGGBB>, <bold>, etc.
prefix: "<gray>[</gray><gold>PHD</gold><gray>]</gray> "
no-permission: "<red>You don't have permission to do this.</red>"
reloaded: "<green>Configuration reloaded.</green>"
help: "<newline><gold><bold>PlayerHeadDrops</bold></gold> <gray>v2.0.0</gray><newline><yellow>/phd reload</yellow> <gray>— reload configuration</gray><newline><yellow>/phd give <player> [receiver]</yellow> <gray>— give a player head</gray><newline><yellow>/phd help</yellow> <gray>— show this menu</gray>"
give-usage: "<red>Usage: /phd give <player> [receiver]</red>"
give-console: "<red>From console, specify receiver: /phd give <player> <receiver></red>"
give-success: "<green>Head of <yellow>%player%</yellow> given to <yellow>%receiver%</yellow>.</green>"
player-not-found: "<red>Player not found or offline.</red>"
unknown: "<red>Unknown subcommand. See /phd help.</red>"
```

</details>

---

## Configuration

<details>
<summary>config.yml (click to expand)</summary>

```yaml
# ─────────────────────────────────────────
#  PlayerHeadDrops v2.0.0  |  Author: Kasperoid
# ─────────────────────────────────────────

config-version: 2

# ── Player heads ─────────────────────────────────────────────────────────────
drop-chance: 1.0
one-time-drop: false
cooldown-seconds: 0
only-pvp: false
drop-to-inventory: false

# ── Anti-farm ────────────────────────────────────────────────────────────────
anti-farm:
  ignore-suicide: true
  ignore-void: false
  ignore-self-kill: true

# ── World restrictions ──────────────────────────────────────────────────────
worlds:
  mode: blacklist
  list:
    - world_the_lobby
    - creative_world

# ── Head name and lore ──────────────────────────────────────────────────────
head:
  name-format: "%player%'s Head"
  name-color: yellow
  name-italic: false
  lore:
    - "<gray>Killed by: <white>%killer%</white></gray>"
    - "<gray>World: <white>%world%</white></gray>"
    - "<dark_gray>%date% %time%</dark_gray>"

# ── Mob heads ────────────────────────────────────────────────────────────────
mob-heads:
  enabled: false
  default-chance: 0.05
  only-player-kill: true
  name-format: ""
  chances:
    ZOMBIE: 0.05
    SKELETON: 0.05
    CREEPER: 0.05
    WITHER_SKELETON: 0.10
    PIGLIN: 0.05
    ENDER_DRAGON: 1.0

# ── Looting boost ────────────────────────────────────────────────────────────
looting-boost:
  enabled: false
  per-level: 0.1

# ── Permission boost ─────────────────────────────────────────────────────────
permission-boost:
  enabled: false
  multiplier: 2.0

# ── Announcements ────────────────────────────────────────────────────────────
announce:
  enabled: false
  message: "<yellow>☠ %player%'s head has dropped!</yellow>"
  radius: -1

# ── Economy (requires Vault) ────────────────────────────────────────────────
economy:
  enabled: false
  reward: 0.0

# ── Effects ──────────────────────────────────────────────────────────────────
effects:
  sound:
    enabled: false
    name: entity.player.levelup
  particles:
    enabled: false
    name: SOUL
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
