# VS Code Config

Minimal, distraction-free VS Code configuration focused on Python, JavaScript
and TypeScript development.

Uses Ruff for Python formatting/linting and Prettier for JavaScript/
TypeScript/JSON formatting, with format-on-save enabled.

## Features

- Distraction-free interface
- No minimap, breadcrumbs, sticky scroll or status bar
- Hidden scrollbars
- Normal line numbers, word wrap enabled
- JetBrains Mono, 16px / 24px line height
- Tokyo Night color theme
- Material Icon Theme + Material Product Icons
- Ruff formatting and linting for Python
- Prettier formatting for JS/TS/JSON
- Format on save
- Error Lens diagnostics
- Better Comments
- Python type checking and auto-import completions
- Telemetry disabled
- VS Code AI chat features disabled

## Requirements

- [Visual Studio Code](https://code.visualstudio.com/)
- [JetBrains Mono](https://www.jetbrains.com/lp/mono/) font

## Required extensions

| Extension | Purpose |
|---|---|
| `enkia.tokyo-night` | Tokyo Night theme |
| `pkief.material-icon-theme` | Material file icons |
| `pkief.material-product-icons` | Material product icons |
| `charliermarsh.ruff` | Python formatting and linting |
| `esbenp.prettier-vscode` | JS/TS/JSON formatting |
| `usernamehw.errorlens` | Inline diagnostics |
| `aaron-bond.better-comments` | Comment highlighting |
| `ms-python.python` | Python support |
| `ms-python.vscode-pylance` | Python language server |
| `ms-python.debugpy` | Python debugging |
| `ms-python.vscode-python-envs` | Python environments |
| `christian-kohler.path-intellisense` | Path autocomplete |
| `dbaeumer.vscode-eslint` | ESLint support |

> GitHub Copilot is intentionally not required by this configuration. AI
> features are disabled in `settings.json`.

## Installation

### 1. Back up your current configuration

**Linux**
```bash
cp ~/.config/Code/User/settings.json ~/.config/Code/User/settings.json.backup
```

**macOS**
```bash
cp ~/Library/Application\ Support/Code/User/settings.json ~/Library/Application\ Support/Code/User/settings.json.backup
```

**Windows (PowerShell)**
```powershell
Copy-Item "$env:APPDATA\Code\User\settings.json" "$env:APPDATA\Code\User\settings.json.backup"
```

### 2. Clone the repository

```bash
git clone https://github.com/Shynobisuikast/vscode-config.git
cd vscode-config
```

### 3. Install the configuration

**Linux**
```bash
cp settings.json ~/.config/Code/User/settings.json
```

**macOS**
```bash
cp settings.json ~/Library/Application\ Support/Code/User/settings.json
```

**Windows (PowerShell)**
```powershell
Copy-Item settings.json "$env:APPDATA\Code\User\settings.json"
```

### 4. Install extensions

The extension list is stored in `extensions.txt`.

**Linux/macOS**
```bash
while read -r extension; do
    code --install-extension "$extension"
done < extensions.txt
```

**Windows (PowerShell)**
```powershell
Get-Content extensions.txt | ForEach-Object {
    code --install-extension $_
}
```

Restart VS Code after installation.

## Configuration

### Python

Python development is configured around:

- Ruff (formatter)
- Pylance
- Debugpy
- Python Environments
- Basic type checking
- Auto-import completions
- Format on save

### JavaScript / TypeScript

Prettier is used for JavaScript, JSX, TypeScript, TSX, JSON and JSONC.
Format on save is enabled.

### Editor

The editor is configured to reduce visual clutter:

- Minimap disabled
- Indentation guides disabled
- Breadcrumbs disabled
- Sticky scroll disabled
- CodeLens disabled
- Status bar disabled
- Scrollbars hidden
- Normal line numbers
- Word wrap enabled

## File structure

```
vscode-config/
├── settings.json
├── extensions.txt
├── README.md
├── LICENSE
└── .gitignore
```

## JSONC

`settings.json` uses JSON with Comments (JSONC). This means comments such as:

```jsonc
// Editor configuration
"editor.fontSize": 16
```

are valid in VS Code but are not valid in strict JSON parsers.

## License

MIT License — see [LICENSE](LICENSE).

Copyright (c) 2026 Shynobisuikast
