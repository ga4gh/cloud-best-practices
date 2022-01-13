# How to contribute to Cloud API specifications

Thank you for taking the time to contribute to the Cloud Work Stream's API specifications: [DRS](https://github.com/ga4gh/data-repository-service-schemas), [WES](https://github.com/ga4gh/workflow-execution-service-schemas), [TRS](https://github.com/ga4gh/tool-registry-service-schemas), and [TES](https://github.com/ga4gh/task-execution-schemas), we appreciate it!

## Semantic Versioning

We use [semantic versioning](https://semver.org/) for Cloud API specs, which determines if your proposed changes impact a major or minor release.

## Issues

Suggested changes to Cloud schemas/protocols should be initiated as **Issues** to allow for discussion and review before committing to code changes. Issues serve as the means for collaborating with the group and discussing contributions that will ultimately lead to changes to the APIs. Examples of the type of issues that can be submitted are:
* Feature requests (e.g. new endpoints)
* Optimizations
* Incorrect information
* Potential security vulnerabilities

Please write up your issue using the [new issue template](#) in this repo.

## Pull Requests

Contribution of spec changes is handled via Github pull requests. See "[Creating a pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)" for a good overview.

To ensure that your code contribution can be reviewed, please follow these rules pertaining to forking, branch creation, and pull request creation:
* All contributors, including those with write access to the main repository, should first fork the repository, and then create a new working branch within their own fork. This prevents the `ga4gh` fork from accumulating too many extraneous branches.
* We follow a GitFlow branch model. **Please read the GitFlow guide linked above, it will give you a great overview of how our branches work. Do not make pull requests to `main`!**

    * Always create branches from `ga4gh/develop`, and create pull requests that merge back into `ga4gh/develop`.
    * Never push or make pull requests to `main`. The spec maintainers will make pull requests to `main` when cutting a release.
    * Branches should be named according to the following pattern: `{branch_type}/issue-{number}-{description}`, where:
        
        * `branch_type` is one of:
            * `feature` - for new features
            * `fix` - for fixing errors
            * `support` - for editorial changes and refactors (of the way the spec is written, not refactors of the API itself)
        * `number` is the issue number that the branch/pull request addresses
        * `description` is a short description of the branch (using snake case)

    * An example branch name could be `feature/issue-123-new-endpoint`
    * If the branch naming convention has been followed correctly, nice things will happen: Github Actions will build human-readable documentation with your proposed changes, and host it at a public URL via **Github Pages**.
    * Make modifications to the spec in your new branch. Once complete, create a **pull request** from your branch to `ga4gh/develop`. Please write up your pull request using the [pull request template](#) in this repo. Choose a reviewer from one of the [API Leads](#) of the specification you are working on.

Some additional notes about pull requests:
* If you have multiple related pull requests, coordinate pull requests across the branch set by making them as simultaneously as possible, and cross referencing them.
* Keep pull requests as small as possible, addressing only what is outlined in the issue and nothing more. Large pull requests are hard to review. Pull requests (and their underlying issues) should be self-contained and incremental.
* The first line of commit messages should be a short (<80 character) summary, followed by an empty line, and then any details you want to include.
* Please follow the syntax and style guidelines to get passed the [linter](#).

## Review Process

Pull requests will be reviewed by one or more API leads, and potentially by driver project contributors with a high stake in the proposed changes. The pull request will also be discussed at the Cloud Work Stream call. Changes may be requested by anyone in the work stream. If the proposed changes raise technical disagreements between work stream members, the work stream leads will lead deliberation at the Cloud call to achieve consensus.