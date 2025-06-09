# pnpm-warning

Minimal reproduction where pnpm warns about `node_modules` being present when running `pnpm add --save-dev` in a workspace.

## To reproduce

Setup:
```shell
corepack enable
pnpm install
```

Add a package:
```shell
pnpm add --save-dev prettier -w
```

Expected behaviour: No warning printed.

Actual behaviour:
```text
WARN `node_modules` is present. Lockfile only installation will make it out-of-date
...
```
