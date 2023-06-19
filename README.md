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
  bump_tag:
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

### bump-and-tag

File `bump-and-tag.yml`, contents:

```yml
name: Bump and Tag

on:
  push:
    branches:
      - main

jobs:
  bump_tag:
    uses: stefan-vatov/gh-workflows/.github/workflows/bump-and-tag.yml@main

```

### js build lint

File `js-build-lint.yml`, contents:

```yml
name: js build lint

on:
  push:
  pull_request:

jobs:
  bump_tag:
    uses: stefan-vatov/gh-workflows/.github/workflows/js-build-lint.yml.yml@main

```
