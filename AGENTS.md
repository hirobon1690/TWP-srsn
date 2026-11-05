# Agent guidelines

These rules apply to every AI coding agent working in this repository (Claude Code, Codex, Copilot, Cursor, Gemini, and others). `CLAUDE.md` is a symlink to this file.

## Commits

- Commit as the agent, not as the human. Set both the author and the committer to the agent's own identity, for example `Claude <noreply@anthropic.com>`.
- End the commit message with a co-author line for the maintainer:

  ```
  Co-Authored-By: hirobon1690 <58695125+hirobon1690@users.noreply.github.com>
  ```

- Do not add a co-author line for the agent itself; the agent is already the author.

Example:

```sh
GIT_COMMITTER_NAME="Claude" GIT_COMMITTER_EMAIL="noreply@anthropic.com" \
  git commit --author="Claude <noreply@anthropic.com>" -m "Summary

Body.

Co-Authored-By: hirobon1690 <58695125+hirobon1690@users.noreply.github.com>"
```

## Pull requests

- Start the PR title with the name of the agent in square brackets, for example `[Claude] Support Sarashina Translate 3.2`. Other agents use their own name, for example `[Codex]`.
- The base branch is `srsn`.

## Branch names

- Don't put the trademark "Sarashina" (in any letter case, for example `sarashina-3.2`) in a branch name. Name the branch after the version or the change, for example `v3.2`.
- Upstream tags such as `v3.2` already exist in this repository. If a branch has the same name as a tag, refer to it as `refs/heads/<name>` in git commands.
