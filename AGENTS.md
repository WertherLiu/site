## Command execution

- Keep shell commands short and single-purpose.
- Do not combine multiple repository inspections with semicolons.
- Prefer `rg` and `rg --files` over recursive `Get-ChildItem`.
- Exclude `.git`, `public`, `resources`, and `themes` from broad searches.
- Check that a path exists before reading it.
- Use a timeout of at most 30 seconds for exploratory commands.
- After a timeout, narrow the search scope; do not immediately repeat the same command.
- Report progress before any potentially long-running operation.

## Pull request workflow

- Make changes on a separate branch.
- Run Quarto for affected qmd sources.
- Run Hugo before opening a pull request.
- Include changed files and verification results in the PR description.
- Never merge directly into main.
