# Releases

## Continuous Deployment

[Continuous Deployment (CD)](https://en.wikipedia.org/wiki/Continuous_deployment) does not have releases by design. Ideally, `main` should always be representing the state of your running application.

If you are developing a web app, this is likely how you should handle things and you should not make releases.

## Shortcomings

For some development workflows, like libraries, it is **necessary** to make releases at a slower pace than for every single PR to main.

The proper `git` solution for this is [tags](https://git-scm.com/book/en/v2/Git-Basics-Tagging) used with [semantic versioning](https://semver.org/). Deployment should only be triggered when a new tag is created.

### Bug fixes

With fixed releases, bugfixes can be necessary. Imo, the best way to fix bugs is to **make a new release** from the trunk.

But if you *really* need to bugfix a specific release, the advised process from [trunk based development](https://trunkbaseddevelopment.com/branch-for-release/#fix-production-bugs-on-trunk) is to:

- Create a [late release branch](https://trunkbaseddevelopment.com/branch-for-release/#late-creation-of-release-branches)

- Fix the bug by [cherry-picking a commit **from the trunk**](https://trunkbaseddevelopment.com/branch-for-release/#cherry-picks-from-the-trunk-to-branch-only)
    - Do **not** commit new code directly to the branch

- After inactivity, the release branch is deleted from the repo
