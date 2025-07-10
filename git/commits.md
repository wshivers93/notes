## Commit message format

### Overview

Prefer to follow the [Coventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification

Spec states that commit messages should be structured as follows:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

In most cases, will just stick to `<type>: <description>`

The available types are:

|Tag|Description|
|----|-----|
|feat|Introduces a new feature or functionality.
|fix |Addresses a bug or issue in the code.
|docs|Changes related to documentation.
|style|Formatting changes that do not affect the code's functionality.
|refactor|Code changes that improve structure without altering behavior.
|test|Adds or modifies tests.
|chore|Routine tasks that do not affect the codebase (e.g., updating dependencies).
|breaking|Indicates a change that introduces backward-incompatible behavior.
|revert|Reverts a previous commit.

### Enforcement
To help enforce this in a repo, can utilize the [commit check](https://github.com/marketplace/actions/commit-check-action) github action. This workflow will analyze the commit message and verify it is in the correct format.

By default the workflow checks for a commit signoff, so either disable that option or use the `--signoff` flag when creating a commit.
