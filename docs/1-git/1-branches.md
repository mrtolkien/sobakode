# Git Branches

## `main`

`main` should be where the most up-to-date code resides. To follow proper [Continuous Integration (CI)](https://en.wikipedia.org/wiki/Continuous_integration) practices, code should regularly be merged into `main`.

### Releases

Releases should be created by tagging a commit.

## Branch names

### Features

`feat/description`

A feature (`feat`) is a piece of code that adds **new** functionality to the code.

The description short but clear:

- `feat/add-user-model`
- `feat/add-testing-ci`
- `feat/new-treemap-color-selector`

### Fixes

`fix/related-issue`

A `fix` is code aimed at fixing issues in **existing** code.

If there was a related [issue](https://docs.github.com/en/issues) opened, its ID should be added to the branch name:

- `fix/10359-text-vertical-alignment`
- `fix/user-model-migration-rollback`
- `fix/dockerfile-source-image-update`

### Drafts

`draft/description`

A draft branch is a Work in Progress (WiP) branch that is not made to be merged into `main`. It should be renamed to `feat/...` or `fix/...` once it's ready for merging. It is still a useful tool to share WiP code with coworkers!

Github has supported [Draft PRs](https://github.blog/2019-02-14-introducing-draft-pull-requests/) for a few years now and is a great complement to that.

## Rationale

### Trunk Based Development

[Trunk Based Development Website](https://trunkbaseddevelopment.com/)

Modern CI/CD pipelines should guarantee that only good code gets merged into `main`. This eliminates the need for a `dev` "buffer" branch that code gets merged to before reaching main. Most modern repos use this setup (`react`, `vscode`, `fastapi`, ...) as well as commit-tagging for releases instead of `release/xx.xx` branches.

### Naming

I have chosen to *not* include usernames in git branches. There should be little name collision if branches are named properly and it hurts readability.
