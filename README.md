# Reusable GH Workflows


## Rust

### Lint & Test

File `lint-test.yml`, contents:

```yml
name: lint & test

on:
  push:
    branches:
      - main
      - staging
      - trying
  pull_request:


jobs:
  lint_test:
    uses: stefan-vatov/gh-workflows/.github/workflows/rust-lint-test.yml@main
    with:
      project_dir: <relative path>

```

### pre-commit hookos

File `pre-commit-hooks.yml`, contents:

```yml
name: hooks

on:
  push:
    branches:
      - main
      - staging
      - trying
  pull_request:


jobs:
  lint_test:
    uses: stefan-vatov/gh-workflows/.github/workflows/pre-commit-hooks.yml@main

```
