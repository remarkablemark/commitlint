# commitlint

[![version](https://badgen.net/github/release/remarkablemark/commitlint)](https://github.com/remarkablemark/commitlint/releases)
[![test](https://github.com/remarkablemark/commitlint/actions/workflows/test.yml/badge.svg)](https://github.com/remarkablemark/commitlint/actions/workflows/test.yml)

:notebook: [Lint commit messages](https://commitlint.js.org/) with GitHub Actions.

## Quick Start

```yaml
- name: Commitlint
  uses: remarkablemark/commitlint@v1
```

## Usage

See [action.yml](action.yml)

**Basic:**

```yaml
steps:
  - uses: remarkablemark/commitlint@v1
```

## Inputs

### `version`

**Optional**: The version. Defaults to `1.2.3`:

```yaml
- uses: remarkablemark/commitlint@v1
  with:
    version: 1.2.3
```

## Contributions

Contributions are welcome!

## License

[MIT](LICENSE)
