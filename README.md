# pre-commit hooks for rust

`pre-commit` provides the `rust` language, which allows us to guarantee the existence of `cargo` and other rust binaries like `rustfmt`.

``` yaml
repos:
  # ...
  - repo: https://github.com/keewis/rust-pre-commit
    hooks:
      - rust-fmt
```

Only `rust-fmt` for now, because other hooks (like linting) require downloading and building the dependencies, which doesn't work on machines without internet (like `pre-commit.ci`).
