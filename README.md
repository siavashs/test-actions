# Testing GitHub Actions & Required status checks

This is not a Go file so it does not trigger the `Go` workflow which has the following condition:
```yaml
name: Go
on:
  pull_request:
    paths:
    - '**.go'
```

But since the `Go / Run Checks` is selected on **Required status checks**, the PR is blocked from merging.

The desired behaviour of the **Required status checks** would be to consider if a PR triggers that specific check before forcing a requirement!
