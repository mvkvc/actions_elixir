# actions_mix_dialyzer

This action runs `mix dialyzer` and caches the the folder containing your PLT files.

## Usage

To include this action in your workflow, add the following lines:

```yaml
jobs:
  ...
    ...
    steps:
    ...
    - uses: actions_mix_dialyzer@v1.0.23-alpha
      with:
        - erlang-version:
        - elixir-version:
        ...
```

The full list of inputs are:

  ```yaml
inputs:
  erlang-version:
    description: Erlang version to use
    required: true
    type: string
  elixir-version:
    description: Elixir version to use
    required: true
    type: string
  path_dialyzer:
    description: Path to the folder containing your PLT files relative to the Mix project root.
    required: false
    type: string
    default: dialyzer
  path:
    description: Path to the root of your Mix project.
    required: false
    type: string
    default: .
  args:
    description: Arguments to pass to `mix dialyzer`.
    required: false
    type: string
    default: ""
```
