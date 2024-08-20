# PHP extensions

## Run GitHub actions locally

For developing github actions act is prepared.

### Requirements

```bash
brew install act gh
```

Copy `.secrets.dist` to `.secrets` and replace the secrets accordingly.
Examples of how to get the correct value are provided, ex. `DSC_USERNAME=$(git config --global user.name)` for your current git username

### Usage

To list all jobs
```bash
act -l
```

To run a specific job
```bash
act -j jobid
```
