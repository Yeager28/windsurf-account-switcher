# Windsurf Switcher by Klevernot

> Seamless multi-account pool manager for Windsurf IDE — auto-rotates before rate limits hit

<p align="center">
  <a href="#features">Features</a> &bull;
  <a href="#installation">Installation</a> &bull;
  <a href="#usage">Usage</a> &bull;
  <a href="#configuration">Configuration</a> &bull;
  <a href="#windsurf-accounts--more">Accounts</a> &bull;
  <a href="#license">License</a>
</p>

---

## Windsurf Accounts & More

**14-day trial accounts, Pro upgrades, bulk deals**

📩 **@klevernot** — [Open Telegram](https://t.me/klevernot)

---

## Features

### Auto-Switch Engine
- **10-layer defense** — monitors quota depletion, rate limits, model tier restrictions, and gRPC capacity in real-time
- **Seamless rotation** — switches to the best account before you notice, preserving your conversation
- **Smart selection** — picks the account with the highest remaining credits, skipping expired or rate-limited ones
- **LRU ordering** — moves used accounts to the back of the pool automatically

### Account Management
- **Batch import** — add accounts from text (email:password, one per line) or JSON
- **Manual switch** — click to instantly rotate to any account
- **Quota monitoring** — real-time daily & weekly quota bars per account
- **Labels** — tag accounts for easy filtering and search

### Device Fingerprint
- **6-ID rotation** — rotates machine ID, storage UUID, and device hashes on every switch
- **Prevent linking** — server sees a fresh device each time, accounts stay isolated
- **One-click reset** — reset fingerprint manually anytime

### Pool Dashboard
- **Health status** — at-a-glance pool health (Healthy / Warning / Critical / Empty)
- **Stats** — available, depleted, rate-limited, expired, total counts
- **Activity log** — timestamped log of all switches, refreshes, and actions

### UI
- **Basecoat + TailwindCSS** — shadcn/ui-quality components in vanilla JS
- **Dark mode** — native dark theme matching VS Code / Windsurf
- **Multi-language** — English, Russian
- **Keyboard shortcuts** — `Ctrl+Shift+S` to switch, `Ctrl+Shift+A` to batch add

---

## Installation

1. Download the latest `.vsix` from [Releases](https://github.com/Yeager28/windsurf-switcher/releases)
2. Open Windsurf / VS Code
3. Press `Ctrl+Shift+P` → `Extensions: Install from VSIX...`
4. Select the downloaded file
5. Restart the editor

---

## Usage

### Adding Accounts

Click the **+** button in the sidebar to open the add dialog. Enter accounts one per line:

```
email1@example.com password1
email2@example.com password2
```

Or import from JSON:

```json
[{"email":"user@example.com","password":"pass123"}]
```

### Switching Accounts

- **Auto** — the engine monitors quota and switches automatically when credits run low
- **Manual** — click any account card to switch to it
- **Smart Rotate** — click the shuffle button to check all accounts and switch to the best one
- **Emergency** — use the panic switch command when you hit a rate limit

### Monitoring Quota

Each account shows daily and weekly quota bars:
- **Green** (>50%) — healthy
- **Yellow** (20-50%) — watch out
- **Red** (<20%) — switch soon

### Filtering & Sorting

- Filter by plan type: **All / Trial / Pro / Free**
- Sort by: quota, days left, plan type, email, newest, oldest
- Search accounts by email, plan, or labels

---

## Configuration

Access via `Settings → Extensions → Windsurf Switcher`:

| Setting | Type | Default | Description |
|---------|------|---------|-------------|
| `wam.autoRotate` | boolean | true | Auto-switch when quota below threshold |
| `wam.autoRotateThreshold` | number | 5 | Quota % below which auto-switch triggers |
| `wam.autoRotateTrialThreshold` | number | 5 | Same, for trial accounts |
| `wam.autoRotateIntervalMinutes` | number | 2 | Background check interval (minutes) |
| `wam.autoRotatePreferHighest` | boolean | true | Pick highest-quota account (not first available) |
| `wam.rotateFingerprint` | boolean | true | Rotate device fingerprint on switch |
| `wam.refreshOnSwitch` | boolean | false | Reload window after manual switch |
| `wam.rotateUsedToEnd` | boolean | true | Move used accounts to end (LRU) |
| `wam.language` | string | en | UI language (en / ru) |
| `wam.clientType` | string | windsurf | Client type (windsurf / windsurf-next) |

---

## License

[MIT](LICENSE) &copy; klevernot

---

<p align="center">
  <sub>Built by <a href="https://t.me/klevernot">@klevernot</a> &bull; 14-day trials · Pro upgrades · Bulk deals</sub>
</p>
