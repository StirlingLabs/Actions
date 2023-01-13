# StirlingLabs/Actions

⚠️ This is a special repo!  It has a private partner at [StirlingLabs/Actions-private](https://github.com/StirlingLabs/Actions-private)


## Our **PUBLIC** GitHub Actions Workflows

- 'dotnetBuild' builds Stirling Labs C# repos that are prepared appropriately:
  - Include [Version.Net](https://github.com/StirlingLabs/Version.Net) (see page for details)
  - Uses [GitHubActionsTestLogger](https://github.com/Tyrrrz/GitHubActionsTestLogger) (`dotnet add package GitHubActionsTestLogger`)
- `dotnetRelease`
- `linter` lints code, including this repo.
- 'metadata' tries to get information about the project.
- `name` tries to get the project name (used by metadata).
- `Threshold` reduces pointless runs if nothing has changed since the last run (use `[forceci]` in commit message to force run).
- `version` tries to ascertain the version of the project (used by metadata).


## GitHub Reuusable Actions

- See GitHub documentation on [Reusable Workflows]](https://github.blog/2022-02-10-using-reusable-workflows-github-actions/) for details.
