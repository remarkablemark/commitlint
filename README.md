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
    steps:
      - name: Checkout repository
        uses: actions/checkout@v4
        with:
          fetch-depth: 0
      - name: Commitlint
        uses: remarkablemark/commitlint@v1
```

## Usage

See [action.yml](action.yml)

**Basic:**

```yaml
- uses: remarkablemark/commitlint@v1
```

## Inputs

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
    version: 18.4.3
```

## Contributions

Contributions are welcome!

## License

[MIT](LICENSE)
