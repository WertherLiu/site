## Command execution

- Keep shell commands short and single-purpose.
- Do not combine multiple repository inspections with semicolons.
- Prefer `rg` and `rg --files` over recursive `Get-ChildItem`.
- Exclude `.git`, `public`, `resources`, and `themes` from broad searches.
- Check that a path exists before reading it.
- Use a timeout of at most 30 seconds for exploratory commands.
- After a timeout, narrow the search scope; do not immediately repeat the same command.
- Report progress before any potentially long-running operation.

## Project structure

- Hugo config: hugo.toml
- Global CSS: static/css/site.css
- Downloads list template: layouts/downloads/list.html
- Downloads article template: layouts/downloads/single.html
- Editable guide sources: content/downloads/**/*.qmd
- Generated Hugo files: content/downloads/**/*.md

## Working rules

- Start with git diff.
- Inspect only files named in the task.
- Do not scan public, resources, themes, or .git.
- Edit qmd instead of matching generated md files.
- Render only the affected qmd file.
- Run Hugo after template or CSS changes.
- Never commit or push unless the user explicitly asks.

## Git workflow

- Work directly on main for routine website updates.
- Run Quarto for affected qmd sources.
- Run Hugo before pushing.
- If verification succeeds and the user explicitly asks to publish, commit and push directly to main.
- Never force push.
- Never push when verification fails.