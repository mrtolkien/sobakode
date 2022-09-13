# Pull Requests

## PR contents

A good PR should include:

- Basic explanation of the feature/fix in the PR body
- New tests
    - `feat` should ideally have 100% coverage of the new code
    - `fix` branches should have at least one new test pertaining to what they are fixing
- Relevant doc
    - Wherever that is stored (see [folders](../../3-folders/1-basic))

## Flow

- Create a PR
- Pass all checks
    - Build
    - Unit tests
    - Integration tests
- Review by the relevant code owner
- Merge to `main`
