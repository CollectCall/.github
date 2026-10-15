# Contributing

Start with the repository's README and any local contribution or agent instructions. They contain the setup, validation, and release details for that project.

## Propose a change

- Link the relevant issue or workitem when one exists, and explain the problem and expected behavior.
- Keep pull requests focused. Describe non-obvious tradeoffs and include relevant documentation updates.
- Use Conventional Commit messages unless the repository instructions specify a different format.

## Branches and pull requests

For CollectCall repositories, `develop` is the default and integration branch when it exists; otherwise `main` remains the default. The default determines the GitHub landing branch, fresh-clone checkout and usual suggested PR target. It does not select a deployment environment.

- With `develop`: create feature/fix branches from the latest `develop` and open PRs back into `develop`.
- Without `develop`: create feature/fix branches from the latest `main` and open PRs into `main`.
- Keep `main` release-ready. Promote development or release work through a PR into `main`, following the repository's product-specific release workflow.
- Bring release fixes and next-cycle version changes back to `develop` through a PR from a temporary branch. Do not push directly to either protected branch, including to synchronize them.
- Use `main` instead of legacy `master` for the repository release branch. Preserve histories during migrations; delete temporary branches only after confirming their work is merged and they are no longer needed.

Two organization rulesets apply to all current and future CollectCall repositories, with no bypass actors:

- [Protect main and develop](https://github.com/organizations/CollectCall/settings/rules/25143759): block deletion and force pushes on both branches.
- [Require pull requests to main and develop](https://github.com/organizations/CollectCall/settings/rules/25143881): require PRs into both branches. This rule does not itself mandate approvals or status checks; additional repository protections still apply.

Check the PR base explicitly. Keep repository-specific branch naming, versioning, validation, staging, packaging and release instructions, while respecting the inherited organization rules. A PR merge or default-branch change is not deployment authorization; follow the repository's deployment approval and execution procedures separately.

## Validate and review

- Run the checks relevant to the change and report the commands and results in the pull request.
- Explain any checks you could not run. For documentation-only changes, check links and rendering and say that runtime tests were not run.
- Include practical verification steps when a change affects users.
- Request review from the repository's declared code owners or maintainers. Follow its release and approval requirements.

## Finish the work

Remove temporary artifacts and stop temporary processes created for the task. Preserve existing and concurrent work, required sources, and reproducible tooling. Keep intentional deliverables in established locations and report necessary leftovers.

For questions, use the repository's support instructions or existing issue tracker.
