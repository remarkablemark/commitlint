# commitlint

[![version](https://badgen.net/github/release/remarkablemark/commitlint)](https://github.com/remarkablemark/commitlint/releases)
[![test](https://github.com/remarkablemark/commitlint/actions/workflows/test.yml/badge.svg)](https://github.com/remarkablemark/commitlint/actions/workflows/test.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

📓 [Lint commit messages](https://commitlint.js.org/) with GitHub Actions.

## Quick Start

```yaml
# .github/workflows/commitlint.yml
name: commitlint
on: push
jobs:
  commitlint:
    runs-on: ubuntu-latest
    permissions:
      contents: read
    steps:
      - name: Commitlint
        uses: remarkablemark/commitlint@v1
        with:
          checkout: true
```

## Usage

Validate last commit message or all commit messages in a pull request:

```yaml
- uses: remarkablemark/commitlint@v1
  with:
    checkout: true
```

See [action.yml](action.yml)

## Inputs

### `checkout`

**Optional**: Whether to checkout the repository:

```yaml
- uses: remarkablemark/commitlint@v1
  with:
    checkout: true
```

Omit this input if the repository has already been checked out with all of the history:

```yaml
- uses: actions/checkout@v4
  with:
    fetch-depth: 0
- uses: remarkablemark/commitlint@v1
```

### `config`

**Optional**: The config to enforce conventional commits. Defaults to [`@commitlint/config-conventional`](https://www.npmjs.com/package/@commitlint/config-conventional):

```yaml
- uses: remarkablemark/commitlint@v1
  with:
    config: '@commitlint/config-angular'
```

### `from`

**Optional**: The lower end of the commit range to lint. Defaults to `HEAD~1`:

```yaml
- uses: remarkablemark/commitlint@v1
  with:
    from: HEAD~
```

### `version`

**Optional**: The version of [`@commitlint/cli`](https://www.npmjs.com/package/@commitlint/cli). Defaults to `latest`:

```yaml
- uses: remarkablemark/commitlint@v1
  with:
    version: 19.8.0
```

## License

[MIT](LICENSE)
