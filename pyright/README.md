# No Nonsense Config for Pyright

This configuration is for [Pyright](https://github.com/microsoft/pyright): Static Type Checker for Python.

[Show the Pyright configuration](./pyproject.toml).

## About the settings

This config turns on strict mode and configures all additional checks that are available as warnings. (So this would be an even stricter mode than strict mode.) Pyright checks are disabled whenever Ruff would offer equivalent functionality - so you don't get duplicate warnings when using Pyright along with Ruff - which you definetly should!

> If you are not a masochist, just lower the `typeCheckingMode` setting to `"standard"`.

### Tips & Thoughts

* To have the pyright CLI recognize your installed dependencies, enter venv first or invoke pyright via `uv run bunx pyright`.
* [BasedPyright](https://docs.basedpyright.com/) is a promising alternative, but Pylance refactoring is up to this date uncontested.
* When using Cursor, you are using BasedPyright anyway - these settings should do, and some day I will also take a look at BasedPyright settings.
* In the future, [ty](https://docs.astral.sh/ty/) will be imho the most promising alternative.
