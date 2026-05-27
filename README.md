<h1 align="center">Windsurf Account Switcher & Manager</h1>

<p align="center"><strong>Multi-account pool manager for Windsurf IDE</strong></p>

<p align="center">
  <a href="#features">Features</a> &nbsp;·&nbsp;
  <a href="#install">Install</a> &nbsp;·&nbsp;
  <a href="#usage">Usage</a> &nbsp;·&nbsp;
  <a href="#settings">Settings</a>
</p>

---

<table align="center" style="border-collapse:separate;border-spacing:0;border:2px solid rgba(34,211,238,0.25);border-radius:14px;overflow:hidden;background:linear-gradient(180deg,#0f172a 0%,#0a0f1e 100%);max-width:520px;width:100%;box-shadow:0 0 40px rgba(34,211,238,0.1),0 0 80px rgba(34,211,238,0.05)">
  <tr>
    <td align="center" style="padding:30px 36px 12px;background:linear-gradient(180deg,rgba(34,211,238,0.08) 0%,transparent 60%)">
      <div style="font-size:24px;font-weight:900;color:#22d3ee;letter-spacing:-0.6px;text-shadow:0 0 30px rgba(34,211,238,0.4),0 2px 4px rgba(0,0,0,0.3)">🛒 Buy Windsurf Accounts &amp; More</div>
    </td>
  </tr>
  <tr>
    <td align="center" style="padding:6px 36px 0">
      <div style="font-size:14px;color:#94a3b8;font-weight:600;letter-spacing:0.2px">14-day trials &nbsp;·&nbsp; Pro upgrades &nbsp;·&nbsp; Bulk deals</div>
    </td>
  </tr>
  <tr>
    <td align="center" style="padding:20px 36px 28px">
      <a href="https://t.me/klevernot">
        <img src="https://img.shields.io/badge/📩 @klevernot-Open Telegram-2AABEE?style=for-the-badge&logo=telegram&logoColor=white" alt="@klevernot on Telegram">
      </a>
    </td>
  </tr>
</table>

<br/>

## Features

| | |
|---|---|
| **Auto-Switch** | Monitors quota, rate limits, model tier, gRPC capacity — rotates before you notice |
| **Smart Selection** | Picks the highest-credit account, skips expired and rate-limited ones |
| **Batch Import** | Add accounts from text or JSON in one click |
| **Quota Bars** | Real-time daily & weekly bars per account — green / yellow / red |
| **Fingerprint Rotation** | 6-ID rotation on every switch — accounts stay isolated |
| **Pool Dashboard** | Health status, stats, and activity log at a glance |
| **Dark Theme** | Matches VS Code / Windsurf native dark mode |
| **Multi-Language** | English, Russian |

## Install

1. Download the latest `.vsix` from [Releases](https://github.com/Yeager28/windsurf-account-switcher/releases)
2. Open Windsurf / VS Code
3. `Ctrl+Shift+P` → **Extensions: Install from VSIX...**
4. Select the downloaded file
5. Restart the editor

## Usage

**Add accounts** — Click **+** in the sidebar, enter one per line:
```
email1@example.com password1
email2@example.com password2
```

**Switch accounts** — Click any account card, or let auto-switch handle it when credits run low.

**Filter & sort** — Filter by plan (Trial / Pro / Free), sort by quota, days, email, or date.

## Settings

Access via `Settings → Extensions → Windsurf Account Switcher`:

| Setting | Default | Description |
|---------|---------|-------------|
| `wam.autoRotate` | `true` | Auto-switch when quota below threshold |
| `wam.autoRotateThreshold` | `5` | Quota % that triggers auto-switch |
| `wam.autoRotateIntervalMinutes` | `2` | Background check interval |
| `wam.autoRotatePreferHighest` | `true` | Pick highest-quota account |
| `wam.rotateFingerprint` | `true` | Rotate device fingerprint on switch |
| `wam.refreshOnSwitch` | `false` | Reload window after manual switch |
| `wam.rotateUsedToEnd` | `true` | Move used accounts to end (LRU) |
| `wam.language` | `en` | UI language (en / ru) |
| `wam.clientType` | `windsurf` | Client type (windsurf / windsurf-next) |

---

<p align="center">
  <sub>Built by <a href="https://t.me/klevernot">@klevernot</a></sub>
</p>
