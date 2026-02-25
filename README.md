<img alt="fish" src="images/clown-fish.png" width="160" align="right">

# fish-shop/install-fish-shell

[![OpenSSF Scorecard](https://img.shields.io/ossf-scorecard/github.com/fish-shop/install-fish-shell?label=OpenSSF%20Scorecard)](https://securityscorecards.dev/viewer/?uri=github.com/fish-shop/install-fish-shell) [![Tests](https://img.shields.io/github/actions/workflow/status/fish-shop/install-fish-shell/test.yml?branch=main&color=brightgreen&label=tests)](https://github.com/fish-shop/install-fish-shell/actions) [![Issues](https://img.shields.io/github/issues/fish-shop/install-fish-shell)](https://github.com/fish-shop/install-fish-shell/issues) [![Dependabot](https://img.shields.io/badge/dependabot-active-brightgreen.svg)](https://github.com/fish-shop/install-fish-shell/network/dependencies) [![License](https://img.shields.io/badge/license-MIT-blue)](https://opensource.org/licenses/mit-license.php) [![fish](https://img.shields.io/badge/fish-3.2.2-blue)](https://fishshell.com)

A GitHub action for installing [fish shell](https://fishshell.com).

<hr>

## Prerequisites

This action has a few dependencies that are generally satisfied by most [GitHub-hosted runners](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners) (`macos-*` and `ubuntu-*` environment variants):

* [GNU Bash](https://www.gnu.org/software/bash/)
* [Homebrew](https://brew.sh) (for `macos-*` runners)
* `apt-add-repository` and `apt-get` (for `ubuntu-*` runners)

## Usage

Add a suitable `uses` step to your GitHub [workflow](https://docs.github.com/en/actions/reference/workflow-syntax-for-github-actions):

```yaml
jobs:
  install-fish-shell:
    runs-on: ubuntu-latest
    steps:
      - name: Install fish shell
        uses: fish-shop/install-fish-shell@v2
```

## Action versions

Use one of the following patterns when specifying the version reference for this action in your workflow (i.e. the `{ref}` value in `uses: fish-shop/install-fish-shell@{ref}`):

| Pattern  | Example   | Description                                                            |
|----------|-----------|------------------------------------------------------------------------|
| `vX`     | `v1`      | the latest `v1.*` release including non-breaking changes and bug fixes |
| `vX.Y`   | `v1.1`    | the latest `v1.1.*` release including bug fixes                        |
| `vX.Y.Z` | `v1.1.0`  | the `v1.1.0` release only                                              |

> [!TIP]
> The recommended pattern is `vX` (e.g. `v2`). This will ensure that the version of the action used in your workflow includes the latest non-breaking changes and bug fixes, and guarantees compatibility with previous versions of that major release number.

Using a `main` branch reference in your workflow is _not_ recommended as this branch may include breaking changes intended for the next major release.

## Other GitHub actions

A number of related composite actions are also available from the [fish-shop](https://github.com/fish-shop) 🐟. Check them out:

* [fish-shop/indent-check](https://github.com/fish-shop/indent-check) - A GitHub action for checking indentation in fish shell files
* [fish-shop/syntax-check](https://github.com/fish-shop/syntax-check) - A GitHub action for syntax checking fish shell files
* [fish-shop/install-plugin](https://github.com/fish-shop/install-plugin) - A GitHub action for installing fish shell plugins
* [fish-shop/install-plugin-manager](https://github.com/fish-shop/install-plugin-manager) - A GitHub action for installing a fish shell plugin manager
* [fish-shop/run-fishtape-tests](https://github.com/fish-shop/run-fishtape-tests) - A GitHub action for running Fishtape tests

## Acknowledgements

* Clown fish icon made by [Freepik](https://www.flaticon.com/authors/freepik) from [www.flaticon.com](https://www.flaticon.com/)

## License

`fish-shop/install-fish-shell` is provided under the terms of the [MIT License](https://opensource.org/licenses/mit-license.php).

## Contact

Email me at [marc.ransome@fidgetbox.co.uk](mailto:marc.ransome@fidgetbox.co.uk) or [create an issue](https://github.com/fish-shop/install-fish-shell/issues).
