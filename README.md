# Action Setup Node and NPM

This action sets up a node and npm environment for use in actions.

## How to set the node version?

Set the engine version in your package.json file.

```json
{
  "engines": {
    "node": "20.x"
  }
}
```

## Inputs

| Name         | Description                                | Default                        |
|--------------|--------------------------------------------|--------------------------------|
| `command`    | The command to run                         | `install --no-audit --no-fund` |
| `cache-name` | The cache name for restoring the npm cache | `npm`                          |

## Outputs

The outputs of this action are the same as the outputs of the [actions/setup-node](https://github.com/actions/setup-node) action.


| Name           | Description                                     |
|----------------|-------------------------------------------------|
| `cache-hit`    | A boolean value to indicate if a cache was hit. |
| `node-version` | The installed node version                      |


## Example usage

```yaml
  - name: Setup Node and NPM
    uses: meza/action-setup-node-npm@v1
    with:
        command: 'ci --no-audit --no-fund'
        cache-name: 'npm-ci' 
```
