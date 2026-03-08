# Drone CI CLI Skill

This repository contains a Codex skill for working with the Drone CI command-line client.

Official documentation:

- `https://docs.drone.io/`
- `https://docs.drone.io/cli/`
- `https://github.com/drone/docs/tree/master/content/cli`

## Install

Create a symlink from this repository's skill folder into `~/.agents/skills`:

```bash
mkdir -p ~/.agents/skills
ln -s "$(pwd)/drone-ci-cli" ~/.agents/skills/drone-ci-cli
```

If you are not running the command from this repository root, replace `$(pwd)/drone-ci-cli` with the absolute path to the local `drone-ci-cli` folder.

If the symlink already exists, remove it first or replace it with:

```bash
ln -sfn "$(pwd)/drone-ci-cli" ~/.agents/skills/drone-ci-cli
```

## Use

Invoke the skill by name:

```text
$drone-ci-cli inspect the latest build for octocat/hello-world
```
