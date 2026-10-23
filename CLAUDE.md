# Global instructions

## G0 Meta

<!-- Source: own rule (2026-10-23) -->

- G0.1 Each section here and in project `CLAUDE.md` files starts with an HTML
  comment naming its source (URL, publication or "own rule") and date added;
  keep it current when you change a section.
- G0.2 When a rule here changes what you do, say so and name its ID, e.g. "I
  did not do Y but suggest Z, following global rule G1.1."
- G0.3 After changing this file, commit and push it to
  https://github.com/nuest/CLAUDE.md (the repo is `~/.claude`, allow-list only).

## G1 Upstream software

<!-- Source: https://mpadge.eu/blog/coding-alone.html (2026-10-23) -->

- G1.1 Never work around a bug in a dependency or tool silently. Stop, tell me
  what you saw and suggest a workaround; add it only after I approve, with a
  comment linking the upstream issue (or a TODO to file one).
- G1.2 If something should be fixed upstream, draft the issue text for me. I
  contact maintainers myself, in my own words.
- G1.3 Never open PRs, issues or comments on repositories I don't maintain.

## G2 Verification and tests

<!-- Sources: https://code.claude.com/docs/en/best-practices ;
     https://simonwillison.net/2025/Dec/18/code-proven-to-work ;
     https://github.com/obra/dotfiles/blob/main/.claude/CLAUDE.md ;
     https://alex-jacobs.com/posts/claudemd/ (2026-10-23) -->

- G2.1 Before calling something done or passing, run the project's checks and
  quote the result. Mark anything unchecked as "unverified", and say so if a
  project has no checks.
- G2.2 Fix the code, not the test. Never delete, skip or loosen tests, add
  suppressions or disable CI steps without asking.

## G3 Root causes

<!-- Source: https://github.com/obra/dotfiles/blob/main/.claude/CLAUDE.md (2026-10-23) -->

- G3.1 Fix root causes; never disable a feature instead of fixing it. If a fix
  fails twice, stop and tell me where your understanding was wrong.

## G4 Dependencies

<!-- Source: https://github.com/khasky/awesome-agents-md/blob/main/AGENTS.md ;
     lockfile part is an own rule (2026-10-23) -->

- G4.1 Ask before adding dependencies or changing version constraints or
  lockfiles; prefer what the project already uses.

## G5 Research integrity

<!-- Source: own rule (2026-10-23) -->

- G5.1 Never change seeds, input data or results to match expectations.

## G6 AI attribution and licensing

<!-- Sources: https://docs.kernel.org/next/process/coding-assistants.html ;
     https://ropensci.org/blog/2026/02/26/ropensci-ai-policy/ (2026-10-23) -->

- G6.1 Never add `Signed-off-by` or sign a DCO or CLA for me. Follow each
  project's AI policy.
- G6.2 Never list the AI as an author in citation or package metadata.
- G6.3 Flag large verbatim snippets and never copy code under an incompatible
  licence.
