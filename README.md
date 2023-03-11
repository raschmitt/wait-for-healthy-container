A simple action to wait for a Docker container untill the health check returns `healthy` or the timeout is exceeded.

# Usage

```yaml
- name: 'Wait until the container is healthy'
  uses: raschmitt/wait-for-healthy-container/@master
  with:
    container-name: name
    timeout: 120
```

# Input Options

| Input          | Description                                                           | Default | Required |
| -------------- | --------------------------------------------------------------------- | ------- | -------- |
| container-name | Name of the container to be waited                                    |         | `true`   |
| timeout        | Limit of seconds to wait for the container to enter a "healthy" state | 120     | `false`  |

# Output Actions

There are no output options for this action.

# Prerequisites

The docker container must have a healthcheck configured for this action to work.

## How to implement a docker container healthcheck

- [Implementing in a docker-compose file](https://docs.docker.com/compose/compose-file/compose-file-v3/#healthcheck)
- [Implementing in a Dockerfile](https://docs.docker.com/engine/reference/builder/#healthcheck)
