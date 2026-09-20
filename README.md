# VS Code Config

My personal Visual Studio Code configuration: a minimal, distraction-free
editor layout with Python (Ruff) and JS/TS (Prettier) formatting on save.

## What's inside

| File | Description |
|------|-------------|
| `settings.json` | User settings |
| `extensions.txt` | List of installed extensions |

## Highlights

- Minimal UI — no minimap, breadcrumbs, sticky scroll, status bar or scrollbars
- JetBrains Mono with ligatures, 16px / 24px line height
- Format on save: Ruff for Python, Prettier for JS/TS/JSON
- Error Lens for inline diagnostics
- Better Comments with custom tags (`!`, `?`, `todo`, `*`)
- Telemetry disabled, AI chat features off

## Requirements

- [Visual Studio Code](https://code.visualstudio.com/)
- [JetBrains Mono](https://www.jetbrains.com/lp/mono/) — the config falls back
  to Fira Code, then to the system monospace font, but it will look different

## Installation

**1. Back up your current settings**

```bash
cp ~/.config/Code/User/settings.json ~/.config/Code/User/settings.json.bak
```

**2. Copy the settings file**

| OS | Path |
|----|------|
| Linux | `~/.config/Code/User/settings.json` |
| macOS | `~/Library/Application Support/Code/User/settings.json` |
| Windows | `%APPDATA%\Code\User\settings.json` |

```bash
git clone https://github.com/<your-username>/vscode-config.git
cd vscode-config
cp settings.json ~/.config/Code/User/settings.json
```

**3. Install the extensions**

```bash
cat extensions.txt | xargs -L1 code --install-extension
```

PowerShell:

```powershell
Get-Content extensions.txt | ForEach-Object { code --install-extension $_ }
```

## Notes

- `settings.json` uses JSONC (comments and trailing commas). This is valid for
  VS Code but will fail a strict JSON parser.
- Settings are personal by definition — feel free to take only the parts you
  want instead of replacing your whole file.

## License

MIT — see [LICENSE](LICENSE).
