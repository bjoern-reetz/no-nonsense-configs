# No Nonsense Config for Ruff

This configuration is for [Ruff](https://docs.astral.sh/ruff/): An extremely fast Python linter and code formatter, written in Rust.

[Show the Ruff configuration](./pyproject.toml).

## About the settings

> we believe that type checkers and linters should be as strict as possible by default. this ensures that the user aware of all the available rules so they can more easily make informed decisions about which rules they don't want enabled in their project.
>
> [basedpyright about better defaults](https://docs.basedpyright.com/latest/benefits-over-pyright/better-defaults/)

This configuration turns on all rules, deselecting [conflicting ones](https://docs.astral.sh/ruff/formatter/#conflicting-lint-rules) and also ignores magic trailing commas in [imports](https://docs.astral.sh/ruff/settings/#lint_isort_split-on-trailing-comma) and [code](https://docs.astral.sh/ruff/settings/#format_skip-magic-trailing-comma).

I dislike magic commas because they introduce a hysteresis effect into formatters, e.g. adding more and more arguments to a function will eventually make formatters wrap them into seperate lines, but with magic trailing comma enabled, removing arguments would never result in collapsing the arguments back to a single line again.
