# Install Project Scaffold for Codex

## Quick Install

```bash
git clone https://github.com/Imit96/imit-dev-plugins.git /tmp/imit-dev-plugins
mkdir -p ~/.codex/skills
cp -r /tmp/imit-dev-plugins/skills/project-scaffold ~/.codex/skills/
rm -rf /tmp/imit-dev-plugins
```

## Verify

```bash
ls ~/.codex/skills/project-scaffold/SKILL.md
```

## Usage

Start a new Codex session and say:

> "I'm building a new project. Scaffold the docs."

Or describe your project and ask Codex to generate the agent config files.
