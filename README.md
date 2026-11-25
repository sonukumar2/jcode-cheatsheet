# jcode cheat sheet (unofficial)

A one-page reference for [jcode](https://github.com/1jehuang/jcode), the open-source terminal coding agent.

> This is an independent, community-made cheat sheet. It is **not** affiliated with or endorsed by the jcode project. The official source of truth is the [jcode repository](https://github.com/1jehuang/jcode).

Commands change between releases. If something here doesn't work, run `jcode --help` in your terminal, or `/help` inside a session, to see what your version supports.

## Install

macOS and Linux:

```bash
curl -fsSL https://jcode.sh/install | bash
```

Windows 11 (PowerShell 5.1 or newer):

```powershell
irm https://jcode.sh/install.ps1 | iex
```

These download a script and run it immediately. To read it first, open the URL in your browser.

Step-by-step version with platform notes: [How to install jcode](https://learnjcode.org/install-jcode/).

## Terminal commands

| Command | What it does |
|---|---|
| `jcode` | Open the interactive terminal interface |
| `jcode --version` | Show the installed version |
| `jcode --help` | List all commands and options |
| `jcode login` | Log in to a provider (OAuth, API key or local credentials) |
| `jcode login openrouter` | Log in to a specific provider |
| `jcode run "your message"` | Run one message and exit |
| `jcode update` | Update to the latest version |
| `jcode usage` | Show usage limits for connected providers |
| `jcode model list` | List model names you can pass to `-m` |
| `jcode provider list` | List provider IDs you can pass to `-p` |
| `jcode provider current` | Show which provider is selected |

Useful options: `-p <provider>`, `-m <model>`, `-C <folder>` (working directory), `--resume`.

## Slash commands (inside a session)

Type `/` to search every command your version has.

### Models and accounts

| Command | What it does |
|---|---|
| `/help` | Show available commands |
| `/model` | See or switch models |
| `/effort` | Check or change reasoning effort |
| `/login`, `/logout` | Connect or disconnect a provider account |
| `/account` | Switch between connected accounts |
| `/usage` | Check provider usage limits |

### Sessions and context

| Command | What it does |
|---|---|
| `/resume` | Reopen an earlier session |
| `/fork` | Branch the conversation into a new window |
| `/transfer` | Hand off a summary to a new session |
| `/compact` | Summarize older messages to free up context |
| `/rewind` | Go back to an earlier message |
| `/clear` | Erase the conversation history |
| `/save`, `/rename` | Bookmark or rename a session |
| `/info`, `/context` | See token details or the full context |

### Working on code

| Command | What it does |
|---|---|
| `/plan` | Get a plan before any changes are made |
| `/test`, `/review` | Check the work, or start a review session |
| `/commit` | Group changes into commits |
| `/commit-push` | Commit, then push |
| `/todos` | Show the todo card |
| `/subagent` | Start a subagent for one task |
| `/swarm` | Turn multi-agent swarm support on or off |
| `/skills` | List loaded and suggested skills |
| `/memory` | Turn long-term memory on or off |

### Interface and troubleshooting

| Command | What it does |
|---|---|
| `/diff` | Cycle how diffs are displayed |
| `/config` | View or edit configuration |
| `/hotkeys` | List keyboard shortcuts |
| `/keys` | Check for shortcut conflicts |
| `/terminal-setup` | Set up your terminal for jcode |
| `/quit` | Close jcode |

## Changing shortcuts

Edit `~/.jcode/config.toml` (or `$JCODE_HOME/config.toml`):

```toml
[keybindings]
open_resume = "alt+r"
side_panel_toggle = "alt+m"
new_terminal = ""   # turned off
```

Run `/hotkeys` afterwards to confirm.

## Before you let an agent run commands

- Work inside a git repository, so you can see and undo changes.
- Read the diff before committing. Be careful with `/commit-push`.
- Keep API keys and secrets out of the files you ask it to work on.

## More guides

- [jcode commands explained](https://learnjcode.org/commands/)
- [How to use jcode](https://learnjcode.org/how-to-use-jcode/)
- [MCP server guide](https://learnjcode.org/jcode-mcp-server/)
- [jcode with Ollama](https://learnjcode.org/jcode-ollama/)

## Corrections

Found something wrong or out of date? Open an issue or a pull request.

## License

MIT. See [LICENSE](LICENSE).
