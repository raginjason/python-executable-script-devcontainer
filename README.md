# Python executable script in a devcontainer

This project creates an executable Python script inside of a [development container](https://containers.dev). While this isn't terribly complicated, getting everything wired up to work correctly on a new project can be a hassle. This project is designed to be an example that can be built off of or referenced by future projects. A few things of note:

* The executable definition can be found under the `project.scripts` table in [pyproject.toml](pyproject.toml)
* The executable script is named `my-proj-cli` and calls the `main()` function in [myproj.cli](src/myproj/cli.py)
* The example Python package is installed editable as defined by `postStartCommand` in [devcontainer.json](.devcontainer/devcontainer.json). This allows for modifications to be made in place without needing to reinstall the package with every file change

# References

* https://packaging.python.org/en/latest/tutorials/packaging-projects/
* https://packaging.python.org/en/latest/guides/writing-pyproject-toml/#creating-executable-scripts
