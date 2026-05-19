# deep-research

A 13-agent academic research pipeline for Claude Code: literature reviews, systematic reviews,
meta-analysis, fact-checking, and Socratic-guided research exploration. A thin wrapper over the
upstream `Imbad0202/academic-research-skills`.

## Architecture

The wrapper skill is thin: it `Read`s the upstream skill, vendored here as a git **submodule**
at `upstream/`, referenced via `${CLAUDE_PLUGIN_ROOT}/upstream/...` so it resolves wherever the
plugin is installed. Upstream is pinned to `841ef8b` (tag `v3.7.0`).

## Install

```bash
claude plugin marketplace add joelpt/joelpt-claude-plugins
claude plugin install deep-research@joelpt-claude-plugins
```

Then restart Claude Code. Requires read access to the private marketplace repo.

## Clone for development

```bash
git clone --recurse-submodules https://github.com/joelpt/claude-plugin-deep-research.git
```

Distributed via the [`joelpt-claude-plugins`](https://github.com/joelpt/joelpt-claude-plugins)
marketplace. Bump `version` (patch minimum) on any change — the marketplace cache is keyed by version.

## License

MIT (wrapper). Upstream submodule retains its own license.
