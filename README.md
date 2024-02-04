# node-pnpm-setup

This GitHub Action contains boilerplate to bootstrap simple NodeJS and PNPM workflows.

## Example usage

```yaml
on:
  - push
  - pull_request

jobs:
  my-job:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v3

      - uses: mylesj/node-pnpm-setup@v1
        with:
          node-version: 20
          pnpm-version: 8

      - name: run tests
        run: pnpm test
```