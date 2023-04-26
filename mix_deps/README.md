# actions_mix_deps

This action runs `mix deps.get` and caches the dependencies.

## Usage

To include this action in your workflow, add the following lines:

```yaml
- uses: actions_mix_deps@v1.0.2-alpha
  with:
    - erlang-version:
    - elixir-version:
    ...
```

The full list of inputs are:

```yaml
inputs:
  erlang-version:
    description: Erlang version to use.
    required: true
    type: string
  elixir-version:
    description: Elixir version to use.
    required: true
    type: string
  path:
    description: Path to the root of the Mix project.
    required: false
    type: string
    default: .
```
