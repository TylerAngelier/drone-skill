# Authentication And Discovery

## Authenticate

Configure the Drone CLI with environment variables before using server-backed commands:

```bash
export DRONE_SERVER=http://drone.example.com
export DRONE_TOKEN=your-personal-token
```

Read the official setup page if the user needs the documented flow:

- Public docs: `https://docs.drone.io/cli/configure/`
- Source page: `https://github.com/drone/docs/blob/master/content/cli/configure.md`

## Discover Commands

Prefer the installed binary over memory:

```bash
drone --help
drone <group> --help
drone <group> <subcommand> --help
```

Use this sequence when the user asks for a command and you need exact syntax:

1. Confirm the command group from `drone --help`.
2. Confirm subcommands with `drone <group> --help`.
3. Confirm flags and required arguments with `drone <group> <subcommand> --help`.
4. Run the command only after the shape matches the current binary.

## Safety Notes

- Prefer read-only inspection commands first: `info`, `ls`, `last`, `view`.
- Treat `add`, `update`, `rm`, `disable`, `repair`, `stop`, `restart`, `approve`, `decline`, `promote`, and `purge` as state-changing.
- If output formatting is available, use `--format` to reduce noise for follow-up parsing or reporting.
- If the installed CLI version differs from examples in the docs, keep the docs for intent and keep local help for exact syntax.
