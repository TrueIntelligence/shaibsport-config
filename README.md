# ShaibSport remote config (easy guide)

Main file: **`live_config.json`**

## What to do when you change something

1. Edit the value in `live_config.json`
2. Change **`version`** at the top: `2` → `3` → `4` … (must go up)
3. Push / save to GitHub
4. App downloads the new file only when `version` is higher

## Important words

| Value | Meaning |
|--------|--------|
| `true` | ON / show |
| `false` | OFF / hide |

## Sections (top → bottom)

1. **`version`** — bump this after every real change  
2. **TAB SWITCHES** — which main tabs show *before* Admin unlock  
3. **FAN TOOLS** — Journal, Lineup, Training, etc. (for App Review)  
4. **TAB NAMES** — Arabic / English labels (keep filled — don’t leave `""`)  
5. **SETTINGS ROWS** — Donate (Red Bull), South Arabia, Contact, Dealzz, etc.  
6. **MATCHES TAB TILES** — `livePlayers`, `browserPlayers`, `domainBrowsers` (needed after unlock)  
7. **CHANNEL URLS** — stream / channel links  
8. **WATCH / MESSAGES / MORE** — other features  

## App Review vs unlock (simple)

- **Before passcode (Apple sees this JSON):** fan tools ON, match tabs OFF  
- **After Admin passcode:** the **app** turns Today / Matches / World Cup / … ON, and hides fan tools  
- So: keep **Matches tiles + tab names filled** even when match tabs are `false` here

## Do NOT

- Don’t set tab names to `""` (empty)  
- Don’t clear `livePlayers` / `browserPlayers` / `domainBrowsers` to `[]` unless you really want an empty Matches tab after unlock  
- Don’t forget to bump **`version`**

## Notes starting with `_`

Keys like `_readme` and `_section_1_tabs` are **comments for you**. The app ignores them.
