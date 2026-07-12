<h1 align="center">        
  AuthX
</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0.0-red?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Java-21-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Paper-1.21+-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Spigot-1.21+-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Folia-Supported-brightgreen?style=for-the-badge" />
  <img src="https://img.shields.io/badge/BungeeCord-Supported-yellow?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Velocity-3.x+-purple?style=for-the-badge" />
  <img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/bStats-32560-purple?style=for-the-badge" />
</p>

<p align="center">
  <b>Advanced multi-platform authentication plugin for Minecraft servers</b><br>
  <sub>🔒 Secure • ⚡ Lightweight • 🗄️ Multi-Database • 🌍 Multi-Language • 🌐 Proxy-Ready</sub>
</p>

---

## 📖 About

AuthX is a high-performance authentication plugin built for modern Minecraft servers. It provides a complete account security solution with premium verification, anti-bot protection, multi-database support, and seamless proxy integration for networks running Velocity or BungeeCord.

Designed for server owners who need **rock-solid security** without sacrificing performance or usability.

---

## ✨ Features

### 🔒 Authentication & Security
- 🔑 **Secure Password Hashing** — BCrypt (default), SHA-256, and PBKDF2 with auto-rehashing
- 🤖 **Anti-Bot / CAPTCHA** — Interactive GUI-based captcha for unregistered players
- ⏱️ **Rate Limiting** — Configurable cooldowns to prevent brute-force attacks
- 💤 **Session Management** — Skip re-login on rejoin with IP-verified sessions
- 🚫 **Max Accounts Per IP** — Prevent multi-account abuse
- 💪 **Password Strength Rules** — Enforce length, mixed case, numbers, and special characters
- 🚫 **Blocked Passwords** — Built-in list of common passwords players cannot use
- 🌐 **IP Change Alerts** — Notifies players when their IP address changes

### 🎮 Premium Integration
- ✅ **Premium Auto-Login** — Verified premium players authenticate automatically
- 🔗 **Premium Linking** — Link cracked + premium accounts via verification code
- 🌐 **Proxy Auto-Detection** — Automatically detects Velocity and BungeeCord
- 🔄 **UUID Migration** — Seamless UUID migration with LuckPerms permission transfer
- 📡 **ProtocolLib Support** — Standalone premium verification without a proxy

### 🗄️ Multi-Database
| Database | Use Case |
|----------|----------|
| 🪶 **SQLite** | Default, zero-config, file-based |
| 🐬 **MySQL** | Production servers, HikariCP connection pooling |
| 🍃 **MongoDB** | Document-based, scalable |
| ⚡ **Redis** | High-speed caching / networks |

### 🌍 Multi-Language (14 Languages)
🇺🇸 English • 🇪🇸 Spanish • 🇫🇷 French • 🇩🇪 German • 🇧🇷 Portuguese • 🇮🇹 Italian • 🇳🇱 Dutch • 🇵🇱 Polish • 🇷🇺 Russian • 🇹🇷 Turkish • 🇨🇳 Chinese • 🇯🇵 Japanese • 🇰🇷 Korean • 🇸🇦 Arabic

### 🌐 Proxy Support
- ⚡ **Velocity** — Full plugin channel support, real UUID capture
- 🔗 **BungeeCord** — Legacy channel support
- 🔄 **Auto-login** — Premium players authenticate through the proxy
- 🔑 **Verification Code System** — Link accounts across proxy sub-servers

### 🎨 Visual Effects
- 👁️ Blindness & speed lock for unauthenticated players
- 📊 Boss bar countdown timer (color changes as time runs out)
- 💬 Action bar reminder
- 📺 Custom login / register / success screen titles
- 👋 Configurable welcome messages with placeholders
- 🔊 Level-up sound on successful authentication

### 📍 Spawn System
- 🛡️ **Auth** — Waiting area while players authenticate
- 🆕 **First Join** — Spawn point on first registration
- ✅ **Join** — Teleport location after successful login
- 💀 **Respawn** — Custom respawn location for authenticated players

### 👑 Moderation & Administration
- ⚙️ **Admin GUI** — Full account settings GUI (`/account`)
- 📋 **Login History** — View last 10 authentication events with IPs
- 📱 **2FA / TOTP** — Time-based one-time passwords via authenticator apps
- 💬 **Discord Webhook Alerts** — Real-time notifications for security events
- 📝 **Comprehensive Logging** — Every auth event logged to database
- ✅ **Whitelist Mode** — Built-in whitelist with add/remove/list management
- 📊 **PlaceholderAPI** — 10+ placeholders for scoreboards, tab lists, and more

### 🖥️ Console
- 🎨 Professional startup output with ASCII banner
- 🌈 Color-coded console messages
- 🔒 Password filter — prevents sensitive commands from appearing in server logs

---

## 📋 Commands

### 👤 Player Commands

| Command | Alias | Description |
|---------|-------|-------------|
| `/login <password>` | `/l` | 🔑 Log in to your account |
| `/register <password> <confirm>` | `/reg` | 📝 Register a new account |
| `/changepassword <old> <new>` | `/cpw` | 🔄 Change your password |
| `/unregister <password>` | `/unreg` | 🗑️ Delete your account |
| `/account` | `/settings`, `/myaccount` | ⚙️ Open account settings GUI |
| `/premium` | `/prem` | 🎮 Premium account linking (proxy only) |
| `/premium confirm <code>` | `/prem confirm` | ✅ Confirm premium linking with code |
| `/axhelp` | `/authxhelp` | ❓ Show all available commands |

### 👑 Admin Commands

| Command | Description |
|---------|-------------|
| `/authx reload` | 🔄 Reload configuration and language files |
| `/authx info` | ℹ️ Show plugin status and info |
| `/authx forcelogin <player>` | 🔐 Force-authenticate a player |
| `/authx forceregister <player> <password>` | 📝 Register a player forcibly |
| `/authx resetpassword <player> <password>` | 🔄 Reset a player's password |
| `/authx lookup <player>` | 🔍 View player auth information |
| `/authx unregister <player>` | 🗑️ Delete a player's account |
| `/authx whitelist <add\|remove\|list\|on\|off>` | ✅ Manage whitelist |
| `/authx spawn <set\|remove\|tp\|list> <type>` | 📍 Manage spawn points |

---

## 🔑 Permissions

| Permission | Default | Description |
|------------|---------|-------------|
| `authx.admin` | `op` | 👑 Access to all `/authx` admin commands |
| `authx.vip` | `false` | ⭐ VIP features: bypass captcha, longer sessions |

---

## ⚙️ Configuration

### 🚀 Quick Start

1. 📦 Drop `AuthX-1.0.0.jar` into your `plugins/` folder
2. 🔄 Restart the server
3. ✏️ Edit `plugins/AuthX/config.yml` to your needs
4. 🔄 Run `/authx reload`

### 📄 config.yml Sections

```yaml
general:
  login-timeout: 60
  max-login-attempts: 5
  restrict-commands: true

language:
  language: en  # en es fr de pt it nl pl ru tr zh ja ko ar

premium:
  enabled: true
  auto-login: true
  verify-timeout: 300

proxy:
  enabled: true  # Auto-detects Velocity / BungeeCord

two-factor:
  enabled: true
  issuer: AuthX

captcha:
  enabled: true
  captcha-timeout: 45

session:
  enabled: true
  duration: 30
  require-same-ip: true

password:
  min-length: 6
  max-length: 64
  require-mixed-case: false
  require-number: false
  require-special-char: false
  block-common-passwords: true

database:
  type: sqlite  # sqlite, mysql, mongodb, redis

effects:
  blindness: true
  titles:
    enabled: true
  boss-bar:
    enabled: true
    color: RED

discord:
  enabled: false
  webhook-url: "WEBHOOK_URL_HERE"

spawns:
  auth: {}
  firstjoin: {}
  join: {}
  respawn: {}
```

---

## 📊 PlaceholderAPI Placeholders

| Placeholder | Description |
|-------------|-------------|
| `%authx_registered%` | ✅ `yes` or ❌ `no` |
| `%authx_authenticated%` | ✅ `yes` or ❌ `no` |
| 🔢 `%authx_logins%` | Total login count |
| 🕐 `%authx_last_login%` | Last login date |
| 📅 `%authx_registered_date%` | Registration date |
| 🌐 `%authx_ip%` | Last known IP address |
| 🎮 `%authx_premium%` | ✅ `yes` or ❌ `no` |
| 🔄 `%authx_premium_autologin%` | ✅ `yes` or ❌ `no` |
| 💤 `%authx_session_enabled%` | ✅ `yes` or ❌ `no` |
| 📱 `%authx_2fa_enabled%` | ✅ `yes` or ❌ `no` |

---

## 📦 Dependencies

| Dependency | Status | Purpose |
|------------|--------|---------|
| 📦 **Paper 1.21+** | 🔴 Required | Server platform |
| 📡 **ProtocolLib 5.3+** | 🟡 Optional | Standalone premium verification |
| 📊 **PlaceholderAPI** | 🟡 Optional | Placeholder expansion |
| 🎯 **LuckPerms** | 🟡 Optional | UUID migration on premium linking |

> 📦 AuthX ships with HikariCP, jBCrypt, and bStats bundled — no extra jars needed.

---

## 💬 Discord Alerts

AuthX can send real-time security notifications to a Discord channel via webhooks.

**🚨 Monitored Events:**
- 🔴 Failed login attempts
- 🌐 IP address changes
- 📝 New registrations
- 🔄 Password resets by admins
- ❌ Premium verification failures
- 🗑️ Account deletions

---

## 📋 Requirements

- ☕ Java 21 or higher
- 🎮 Minecraft server 1.21.1+ (Paper recommended)

---

## 🖥️ Supported Software

| Software | Versions | Notes |
|----------|----------|-------|
| 📄 **Paper** | 1.21.1 — 1.26+ | ✅ Fully supported (recommended) |
| 🔧 **Spigot** | 1.21.1 — 1.26+ | ✅ Fully supported |
| 🔗 **BungeeCord** | Latest | ✅ Proxy auto-detection & premium linking |
| ⚡ **Velocity** | 3.0.1 — 3.3.0+ | ✅ Proxy auto-detection & premium linking |
| 🍃 **Folia** | 1.21.1+ | ⚠️ Partial support (uses Bukkit scheduler compat layer) |

---

## 📊 Statistics

<p align="center">
  <a href="https://bstats.org/plugin/bukkit/AuthX/32560">
    <img src="https://bstats.org/signatures/bukkit/AuthX/32560.svg" alt="AuthX bStats" width="400" />
  </a>
</p>

> 📈 [View full statistics on bStats](https://bstats.org/plugin/bukkit/AuthX/32560)

---

## 🆘 Support

- 🐛 **Issues:** [GitHub Issues](https://github.com/your-repo/AuthX/issues)
- 💬 **Discord:** [Join our Discord](https://discord.gg/securityx)
- 🌐 **Website:** [securityx.sbs](https://securityx.sbs)

---

<p align="center">
  🔨 Built with passion by <b>SecurityX</b><br>
  <sub>⭐ If you enjoy AuthX, consider leaving a star on GitHub!</sub>
</p>
