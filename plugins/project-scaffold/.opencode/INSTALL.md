# Install Project Scaffold for OpenCode

## Quick Install

```bash
git clone https://github.com/Imit96/imit-dev-plugins.git /tmp/imit-dev-plugins
mkdir -p ~/.opencode/skills
cp -r /tmp/imit-dev-plugins/skills/project-scaffold ~/.opencode/skills/
rm -rf /tmp/imit-dev-plugins
```

## Verify

```bash
ls ~/.opencode/skills/project-scaffold/SKILL.md
```

## Usage

Start a new OpenCode session and say:

> "I'm building a new project. Scaffold the docs."

Or describe your project and ask the agent to generate the config files.
