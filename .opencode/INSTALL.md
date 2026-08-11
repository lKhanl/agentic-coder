# Installing agentic-coder for OpenCode

## Prerequisites

- [OpenCode.ai](https://opencode.ai) installed

## Installation

Add agentic-coder to the `plugin` array in your `opencode.json` (global or project-level):

```json
{
  "plugin": ["agentic-coder@git+https://github.com/lKhanl/agentic-coder.git"]
}
```

Restart OpenCode. The plugin installs through OpenCode's plugin manager and
registers the skill.

Verify by asking: "Are you following agentic-coder rules?"

OpenCode uses its own plugin install. If you also use Claude Code or Codex,
install agentic-coder separately for each one (see the root [README](../README.md)).

## Usage

Use OpenCode's native `skill` tool:

```
use skill tool to list skills
use skill tool to load agentic-coder
```

The plugin also injects the skill's rules into the first message of every
session, so the approval-gated workflow is active immediately.

## Updating

OpenCode installs agentic-coder through a git-backed package spec. If updates
don't appear after a restart, clear OpenCode's package cache or reinstall the
plugin.

## Troubleshooting

### Plugin not loading

1. Check logs: `opencode run --print-logs "hello" 2>&1 | grep -i agentic-coder`
2. Verify the plugin line in your `opencode.json`
3. Make sure you're running a recent version of OpenCode
