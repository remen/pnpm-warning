# pnpm-warning

Minimal reproduction of pnpm's

## To reproduce

Setup
```shell
corepack enable
pnpm install
```

# Add a package
```shell
pnpm add --save-dev prettier -w
```

```text
WARN `node_modules` is present. Lockfile only installation will make it out-of-date
...
```
