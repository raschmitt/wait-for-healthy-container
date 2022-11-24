A simple action to wait for a Docker container till the health check returned ''healthy'' or the timeout is exceeded.

# Usage

```yaml
- name: 'Wait until the container is healthy'
  uses: raschmitt/wait-for-healthy-container/@v1
  with:
    container-name: name
    timeout: 120
```

# Input Options

| Input | Description | Default | Required |
| ----- | ----- | ----- | ----- |
| container-name | Name of the container to be waited | | `true` |
| timeout | Limit of seconds to wait for the container to enter a "healthy" state | 120 | `false` |

# Output Actions

There are no output options for this action.
