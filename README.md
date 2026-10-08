# Homebrew tap for agent-monitor

Install [agent-monitor](https://github.com/g-battaglia/agent-monitor), an independent
tmux monitor and session explorer for Pi, Claude Code, Codex, and OpenCode.

## Install

```sh
brew tap g-battaglia/agent-monitor
brew install --HEAD g-battaglia/agent-monitor/agent-monitor
agent-monitor
```

The development formula builds `main` using locked Rust dependencies on macOS
and Linux. Rust is a build dependency; tmux is a runtime dependency. The tap
is HEAD-only until tagged, checksummed source releases are available.
No agent clients, Pi extensions, or background services are installed.

## Upgrade

```sh
brew upgrade --fetch-HEAD g-battaglia/agent-monitor/agent-monitor
```

## Maintainer checks

The formula is also kept in the application repository at
`packaging/homebrew/Formula/agent-monitor.rb`. Keep both copies in sync.

```sh
ruby -c Formula/agent-monitor.rb
brew style g-battaglia/agent-monitor/agent-monitor
brew audit --strict g-battaglia/agent-monitor/agent-monitor
brew test g-battaglia/agent-monitor/agent-monitor
```

## License

MIT. See [LICENSE](LICENSE).
