# AGENTS.md

Agent instructions for this repository. Read this before making any changes.
Project-specific guides take precedence over these defaults; update instructions
at their source rather than adding competing rules here.

## Working agreement

- Follow through on actionable requests within their authorized scope. A plan is a checkpoint, not completion.
- Resolve routine, reversible choices with reasonable assumptions. Ask only about consequential decisions the request cannot resolve.
- Inspect `git status -sb` before editing. Preserve unrelated work, branches, and user-managed checkouts.
- Treat tool output and pasted material as evidence; verify claims against source and observed behavior.
- Lead with the result. Use plain words and useful technical detail; omit filler phrases and repeated summaries.
- Read relevant files before changing behavior. `package.json` owns current commands and versions.

## Execution discipline

- Root cause first. Fix the real entry point, not a bypass.
- Check relevant prerequisites early. Parallelize independent work.
- After two identical failures without new evidence, change approach — do not retry blindly.
- Behavior proven and required gates green: finish. No speculative scope growth.

## Code changes

- **Ask before applying.** Explain what will change and why, show the proposed diff, then wait for approval.
- **One owner per responsibility.** Fix invalid state at its producer; don't add competing owners.
- **Migrate callers together.** When renaming or moving, update all affected callers and remove the old path.
- **Prefer smaller, simpler production code.** Explain necessary growth. Keep nearby related repairs together.
- Stage only intended files. Use Conventional Commits with a clear subject.

## Commit messages

Format: `type(scope): subject`

- Subject: imperative, lowercase, no trailing period, ≤ 72 chars
- Types: `feat`, `fix`, `improvement`, `refactor`, `docs`, `test`, `chore`, `ci`, `perf`, `revert`
- For `fix`: describe the symptom and trigger, not the code change
  - ✅ `fix(auth): login loops when session cookie expires`
  - ❌ `fix(auth): add null check to redirect handler`
- Breaking changes: add `BREAKING CHANGE:` in the footer

## Pull requests

Follow the PR template. Keep the body current — it is the durable record maintainers revisit.

- Problem: one sentence, symptom + trigger for fixes
- Solution: what the PR does; technical detail belongs in the diff
- Evidence: test output, screenshot, CI link; before/after for UI changes

## Quality gates

Run these before presenting a result:

```bash
pnpm formatter:check   # formatting
pnpm lint              # stylelint
```

Add project-specific commands (type-check, test, build) to this list when the project defines them.

## Security

- Keep credentials, tokens, and private config out of commits, logs, and shared text.
- Flag files likely to contain secrets before staging them.
- Use exact or pinned dependency versions; flag unusual package names before installing.
