# Influxdata CPython WASI Build

Fork of [`https://github.com/brettcannon/cpython-wasi-build`](https://github.com/brettcannon/cpython-wasi-build).

## Creating a Release

If you wish to create a release for a new version of CPython, follow these steps:

- Update `PYTHON_MAJOR_MINOR` in `.github/workflows/release.yml` to the desired version
- Fetch the corresponding upstream branch for the release
  - Add the upstream `brettcannon/cpython-wasi-build` repository as a remote  
    ```
        git remote add brett-cannon https://github.com/brettcannon/cpython-wasi-build
    ```
  - Switch to the release branch for the version you are releasing (e.g., `release/3.12`), and push it up to the forked
    remote
    ```
        git fetch brett-cannon
        git switch -c release/3.12 brett-cannon/release/3.12
        git push -u origin release/3.12
    ```
- Create a new release via the GitHub UI, ensuring to include a Python micro version for the level of release you wish to create (e.g., `3.12.0`, `3.12.1`, etc.)