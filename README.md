# Setup Test Splitter

Installs the [Buildkite Test Splitter](https://github.com/buildkite/test-splitter) for use in [Buildkite](https://buildkite.com) builds.

## Example

```yaml
steps:
- name: RSpec
  plugins:
  - sj26/setup-test-splitter
  command: test-splitter 
  parallelism: 10
  env:
    BUILDKITE_SPLITTER_SUITE_SLUG: my-suite
    BUILDKITE_SPLITTER_API_ACCESS_TOKEN: my-secret-token
```

## Select test-splitter version to install

By default, the latest released version of Test Splitter will be installed.

You can select a version with the version parameter:

```yaml
steps:
- plugins:
  - sj26/setup-crane:
      version: v0.7.2
  command: test-splitter --version
```
