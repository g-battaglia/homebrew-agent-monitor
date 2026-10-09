# Homebrew tap for tmux-agent-monitor

Install [tmux-agent-monitor](https://github.com/g-battaglia/tmux-agent-monitor),
a tmux-native monitor and session explorer for **Claude Code, Codex, OpenCode,
and Pi**. Track live agents, inspect local history, and resume conversations
without adding another terminal platform.

## Install

```sh
brew tap g-battaglia/tmux-agent-monitor
brew install --HEAD g-battaglia/tmux-agent-monitor/tmux-agent-monitor
tmux-agent-monitor
```

The formula builds upstream `main` with locked Rust dependencies. Rust is a
build dependency; tmux is a runtime dependency. It does not install agents,
Pi extensions, services, or background processes. Installation is HEAD-only
until upstream publishes a tagged, checksummed release.

## Upgrade

```sh
brew upgrade --fetch-HEAD g-battaglia/tmux-agent-monitor/tmux-agent-monitor
```

## Rename compatibility

The application was previously named `agent-monitor` and this tap was
`homebrew-agent-monitor`. GitHub redirects preserve old repository URLs.
`Aliases/agent-monitor` resolves to the canonical formula; the installed
command is `tmux-agent-monitor`, not a second legacy executable.

Existing catalog data is preserved by the application. See upstream's
[rename compatibility notes](https://github.com/g-battaglia/tmux-agent-monitor#rename-compatibility)
for state directories, environment aliases, and optional Pi observers.

## Maintenance

The formula and alias are mirrored in upstream `packaging/homebrew/`.
Keep both copies synchronized; do not add CI workflows or user-specific paths.

```sh
brew style g-battaglia/tmux-agent-monitor/tmux-agent-monitor
brew audit --strict g-battaglia/tmux-agent-monitor/tmux-agent-monitor
```
