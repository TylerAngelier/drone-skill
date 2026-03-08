# Command Map

This map is based on the installed `drone` CLI observed when the skill was created. Re-check with `drone --help` and `drone <group> --help` before relying on it.

## Top-Level Commands

- `build`: manage builds
- `cron`: manage cron jobs
- `log`: manage logs
- `encrypt`: encrypt a secret
- `exec`: execute a local build
- `info`: show information about the current user
- `repo`: manage repositories
- `user`: manage users
- `secret`: manage secrets
- `server`: manage servers
- `queue`: queue operations
- `orgsecret`: manage organization secrets
- `autoscale`: manage autoscaling
- `convert`: deprecated no-op for legacy format conversion
- `lint`: lint the yaml file
- `sign`: sign the yaml file
- `jsonnet`: generate `.drone.yml` from jsonnet
- `starlark`: generate `.drone.yml` from starlark
- `plugins`: plugin helper functions
- `template`: manage templates

## Observed Grouped Subcommands

### `build`

- `ls`
- `last`
- `info`
- `create`
- `stop`
- `restart`
- `approve`
- `decline`
- `promote`
- `rollback`
- `queue`
- `queue-v2`

### `repo`

- `ls`
- `info`
- `enable`
- `update`
- `disable`
- `repair`
- `chown`
- `sync`

### `secret`

- `add`
- `rm`
- `update`
- `info`
- `ls`

### `template`

- `add`
- `info`
- `ls`
- `update`
- `rm`

### `log`

- `purge`
- `view`

## Useful Discovery Commands

```bash
drone build info --help
drone repo update --help
drone secret add --help
drone template info --help
drone exec --help
```
