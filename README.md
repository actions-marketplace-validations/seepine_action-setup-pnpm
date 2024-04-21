# actions-setup-pnpm

> Use corepack, if you want to set pnpm version, setting the packageManager field in package.json like `"packageManager":"pnpm@8.10.2"`

## Usage

It will setup pnpm and run `pnpm install`.

```yml
- name: Setup pnpm and Install
  uses: seepine/actions-setup-pnpm@v1
```

## Input

| Output Item  | Description                                                                                            | Required | Default |
| ------------ | ------------------------------------------------------------------------------------------------------ | -------- | ------- |
| run_install  | If specified, run pnpm install.                                                                        | false    | true    |
| install_cmd | Default install cmd is <pnpm install --frozen-lockfile --prefer-offline>                                | false    | -       |
| enable-corepack | Enable corepack, not use pnpm/action-setup action                                                   | false    | true    |
| verison     | Only enable-corepack false, If you're not setting the packageManager field in package.json, set the version here | false | 8 |
| cwd          | Changes node's process.cwd() if the project is not located on the root. Default to process.cwd() files | false    | .       |
