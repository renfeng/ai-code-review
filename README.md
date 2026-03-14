# ai-code-review

This project has moved to GitLab: https://gitlab.com/renfeng.cn/ai-code-review-kirospace

## Why the move?

This repo was originally used as the source for a [Kiro Power](https://kiro.dev/docs/powers/) installed via "Add power from GitHub." However, powers installed from GitHub don't update when the source repo changes ([Kiro#6278](https://github.com/kirodotdev/Kiro/issues/6278)). The only way to get updates is to uninstall and reinstall the power manually.

Beyond powers, Kiro's other distribution mechanisms also have limitations for GitHub-hosted repos:

- **Skills** — imported from GitHub are copied into the local `.kiro/skills/` directory. There is no update or sync mechanism; re-importing overwrites the local copy, but there's no notification when the source changes.
- **Custom agents** — defined in `.kiro/agents/` within a workspace. There is no way to distribute or install a custom agent from a remote source. Each user must create their own copy.

Since the npm package (`@renfeng/ai-code-review`) is the reliable delivery channel for the MCP servers, and the Kiro Power now references the npm package rather than this repo, there's no reason to maintain a GitHub copy.
