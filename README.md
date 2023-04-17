# Reusable GH Workflows


## Rust

### Lint & Test

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
    uses: https://github.com/stefan-vatov/gh-workflows/.github/workflows/rust-lint-test.yml
    with:
      project_dir: <relative path>
  
```

