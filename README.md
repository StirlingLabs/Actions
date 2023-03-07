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

## Coding Recommendations

- Break up steps as much as you can, practically.  This makes it easier for users to see what has happened.
- `echo` enough to make sure a user can see what has gone wrong.  Be a bit more verbose than you might assume, because users won't have as much context as you do when writing it.
- Use bash as your shell unless forced not to by some important external requirement.
  - `default: ... shell: bash` is generally available and should be used whenever possible (default `env` is nice sometimes, too).
- Within steps:
  - `env` comes before `run`
  - Use bash functions to organise code
    - At least `main() {}`
  - End bash scripts with at least `exit` but ideally `main "$@" ; exit`.  This makes it easy to see the end of the script within the Action (amoung other benefits).
- camelCase variables.  Just because that's what's there.
- Lint all Actions.