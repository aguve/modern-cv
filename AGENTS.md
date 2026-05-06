# AGENTS.md

Static HTML/CSS CV site. No build step, no dependencies, no test suite.

- Open `index.html` directly in a browser to preview
- `opencode.json` and `cvAndreuGuzman.txt` are gitignored intentionally
- Uses Google Fonts (Inter) via CDN, no local font files
- Plain HTML/CSS, no framework

## Git
- Commit only when explicitly requested by the user
- Commit messages: concise, present tense, describe the exact change (e.g., "Update name to Andreu Guzman")
- Never force push to main; warn user if requested
- Push to remote only when explicitly asked

### Push Credentials
- Credentials stored in `.git-credentials` (gitignored, never commit this file)
- File contains: `GIT_USERNAME` and `GIT_TOKEN`
- When pushing:
  1. Read `.git-credentials` to get username and token
  2. Set remote URL with credentials: `git remote set-url origin https://<USERNAME>:<TOKEN>@github.com/aguve/modern-cv.git`
  3. Run `git push`
  4. Remove credentials from URL: `git remote set-url origin https://github.com/aguve/modern-cv.git`

- Commit Types:
Type     Purpose
feat     New feature
fix     Bug fix
docs     Documentation only
style     Formatting/style (no logic)
refactor     Code refactor (no feature/fix)
perf     Performance improvement
test     Add/update tests
build     Build system/dependencies
ci     CI/config changes
chore     Maintenance/misc
revert     Revert commit
- Generate Commit Message
    Type: What kind of change is this?
    Scope: What area/module is affected?
    Description: One-line summary of what changed (present tense, imperative mood, <72 chars). Suggest one or two, but let the user write one if wants.

- Execute Commit

# Single line
git commit -m "<type>[scope]: <description>"