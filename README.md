# LOGZ TeamBalance

**LOGZ TeamBalance** is a CounterStrikeSharp / CS2 plugin that keeps teams balanced on LOGZ Romania servers.

The plugin is designed to be simple, safe and lightweight. It can balance teams on round start or after team changes, with options for admin immunity, warmup protection and dead-player preference.

---

## Current Version

```txt
1.0.0
```

---

## Features

- automatic team balancing
- balance on round start
- balance after player team changes
- manual balance command
- minimum player count
- maximum allowed team difference
- warmup ignore option
- admin/root immunity
- preferred dead-player movement
- optional top-fragger protection
- chat messages
- center message for moved player
- version/info commands
- `version.txt` support
- GitHub update URL support
- LOGZ Romania proprietary license

---

## Commands

```txt
css_logzbalance
css_logzbalance_status
css_logzbalance_version
css_logzbalance_info
css_logzbalance_reload
```

### Command Details

| Command | Description |
|---|---|
| `css_logzbalance` | Forces a team balance check |
| `css_logzbalance_status` | Shows current team counts and status |
| `css_logzbalance_version` | Shows plugin version and version URL |
| `css_logzbalance_info` | Shows plugin info, GitHub URL, website and license |
| `css_logzbalance_reload` | Shows the correct reload command |

---

## Permission

Default permission:

```txt
@logz/teambalance
```

Optional immunity permission:

```txt
@logz/balanceimmune
```

Root permissions also have access automatically:

```txt
@css/root
@logz/root
```

---

## Installation

1. Compile the plugin with Visual Studio 2022.
2. Copy the compiled files to:

```txt
/game/csgo/addons/counterstrikesharp/plugins/LOGZ_TeamBalance/
```

3. Make sure the folder contains:

```txt
LOGZ_TeamBalance.dll
version.txt
```

4. Restart the server or reload the plugin:

```txt
css_plugins reload LOGZ_TeamBalance
```

---

## Config Path

The config is generated automatically at:

```txt
/game/csgo/addons/counterstrikesharp/configs/plugins/LOGZ_TeamBalance/LOGZ_TeamBalance.json
```

---

## Default Config Example

```json
{
  "Enabled": true,
  "ChatPrefix": "{Gold}[LOGZ Balance]{Default}",
  "WebsiteUrl": "https://www.logz.ro",
  "GithubUrl": "https://github.com/USERNAME/LOGZ_TeamBalance",
  "VersionUrl": "https://raw.githubusercontent.com/USERNAME/LOGZ_TeamBalance/main/version.txt",
  "LicenseName": "LOGZ Romania Proprietary License",
  "CommandPermission": "@logz/teambalance",
  "ImmunePermission": "@logz/balanceimmune",
  "RootImmune": true,
  "AdminsImmune": false,
  "MinPlayers": 4,
  "MaxTeamDifference": 1,
  "BalanceOnRoundStart": true,
  "BalanceDelayAfterRoundStart": 2.0,
  "BalanceOnPlayerTeam": true,
  "PlayerTeamBalanceDelay": 1.5,
  "IgnoreWarmup": true,
  "PreferDeadPlayers": true,
  "DoNotMoveTopFragger": true,
  "ShowChatMessages": true,
  "ShowCenterMessageToMovedPlayer": true
}
```

---

## version.txt

Recommended format:

```txt
1.0.0
https://github.com/USERNAME/LOGZ_TeamBalance
```

After creating your GitHub repository, replace `USERNAME` with your GitHub username or organization.

Example:

```txt
1.0.0
https://github.com/LOGZRomania/LOGZ_TeamBalance
```

Then update the config:

```json
"VersionUrl": "https://raw.githubusercontent.com/LOGZRomania/LOGZ_TeamBalance/main/version.txt"
```

---

## Recommended Settings

For public CS2 servers, recommended:

```json
"MinPlayers": 4,
"MaxTeamDifference": 1,
"BalanceOnRoundStart": true,
"BalanceOnPlayerTeam": true,
"PreferDeadPlayers": true,
"DoNotMoveTopFragger": true,
"IgnoreWarmup": true
```

---

## Reload Notes

For real reload, use:

```txt
css_plugins reload LOGZ_TeamBalance
```

The command:

```txt
css_logzbalance_reload
```

only prints the correct reload instruction.

This avoids `Config.Reload()` API problems on different CounterStrikeSharp versions.

---

## Recommended GitHub Structure

```txt
LOGZ_TeamBalance/
├── LOGZ_TeamBalance.cs
├── LOGZ_TeamBalance.csproj
├── README.md
├── LICENSE.md
└── version.txt
```

---

## License

This project is licensed under the **LOGZ Romania Proprietary License**.

Redistribution, resale, reuploading, leaking, or claiming ownership of this plugin is not allowed.

See [LICENSE.md](LICENSE.md) for details.

---

## Credits

Created for **LOGZ Romania**.

Website:

```txt
https://www.logz.ro
```
