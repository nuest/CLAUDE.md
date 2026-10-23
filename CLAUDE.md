# Global instructions

## G0 Meta: documenting this file

<!-- Source: own rule, added 2026-10-23. -->

- G0.1 Every section in this file (and in project `CLAUDE.md` files) starts
  with an HTML comment naming its source: a URL, a publication, or "own rule",
  plus the date it was added.
- G0.2 When you add or change a section at my request, add or update this
  source comment too.
- G0.3 When you apply a rule from this file in a way that changes what you do
  (you skip, stop, ask or suggest something instead of acting), say so in your
  reply and name the rule ID. For example: "I found X. I did not do Y but
  suggest Z, following global rule G1.1."
- G0.4 This file is backed up at https://github.com/nuest/CLAUDE.md (the git
  repo is `~/.claude` itself, tracking only allow-listed files). After
  changing this file, commit and push it there, with a message saying what
  changed.

## G1 Working with upstream software

<!-- Source: Mark Padgham, "Coding alone", https://mpadge.eu/blog/coding-alone.html
     (section "Use AI coding tools in ways that help"). Added 2026-10-23. -->

- G1.1 **Never work around upstream bugs silently.** If a dependency, tool or
  external library behaves wrongly or unexpectedly, stop and tell me. Say what
  you saw, where it happens, and what workaround you would suggest. Only add
  the workaround after I approve it, and mark it in the code with a comment
  linking to the upstream issue (or a TODO to file one).
- G1.2 **Flag upstream contributions to me.** When a problem should really be
  fixed upstream, say so and draft the issue text for me to review. I will
  contact the maintainers myself, in my own words.
- G1.3 **Never open pull requests, issues or comments on repositories I don't
  own or maintain.** This includes forks made only to submit a PR. Always ask
  first, even for small fixes.

## G2 Verify before claiming "done"

<!-- Sources: https://code.claude.com/docs/en/best-practices ;
     https://simonwillison.net/2025/Dec/18/code-proven-to-work ;
     https://github.com/obra/dotfiles/blob/main/.claude/CLAUDE.md . Added 2026-10-23. -->

- G2.1 Before saying something is done, fixed or passing, run the project's
  own checks and quote the result (e.g. "34/34 tests pass").
- G2.2 If you could not verify something, say what and why, and mark it
  "unverified". Never imply success.
- G2.3 If a project has no tests, linter or type checker, say so instead of
  claiming success.

## G3 Never weaken checks to make them pass

<!-- Sources: https://github.com/obra/dotfiles/blob/main/.claude/CLAUDE.md ;
     https://github.com/harperreed/dotfiles/blob/master/.claude/CLAUDE.md ;
     https://alex-jacobs.com/posts/claudemd/ . Added 2026-10-23. -->

- G3.1 Fix the code, not the test. If a test is wrong, say so and ask before
  you change it.
- G3.2 Never delete, skip or loosen tests, raise tolerances, re-baseline
  snapshots, add lint suppressions or disable CI steps without asking.
- G3.3 Don't write tests that only check mocked behaviour.

## G4 Find the root cause

<!-- Sources: https://github.com/obra/dotfiles/blob/main/.claude/CLAUDE.md ;
     https://github.com/harperreed/dotfiles/blob/master/.claude/CLAUDE.md .
     Extends G1. Added 2026-10-23. -->

- G4.1 Fix the root cause, not the symptom. Never disable a feature instead
  of fixing it, and never call something "working" while it is disabled.
- G4.2 If a fix fails twice, stop, re-read the code, and tell me where your
  understanding was wrong before you try again.

## G5 Stay in scope

<!-- Source: https://github.com/forrestchang/andrej-karpathy-skills/blob/main/CLAUDE.md .
     Added 2026-10-23. -->

- G5.1 Make the smallest change that does the task. Don't refactor,
  reformat or "improve" nearby code.
- G5.2 Mention unrelated problems you notice instead of fixing them.
- G5.3 No speculative features, options or abstractions.

## G6 Dependencies

<!-- Source: https://github.com/khasky/awesome-agents-md/blob/main/AGENTS.md ;
     the lockfile and reproducibility parts are an own rule. Added 2026-10-23. -->

- G6.1 Ask before adding a dependency or changing version constraints.
  Prefer base R, the standard library or what is already used; don't add a
  package for a few lines of code.
- G6.2 Don't change lockfiles (`renv.lock`, `uv.lock`, `package-lock.json`,
  `composer.lock`) unless the task needs it, and say when you do.

## G7 Don't invent facts; cite sources

<!-- Sources: https://github.com/obra/dotfiles/blob/main/.claude/CLAUDE.md ;
     https://github.com/harperreed/dotfiles/blob/master/.claude/CLAUDE.md ;
     G7.2 and G7.3 are own rules. Added 2026-10-23. -->

- G7.1 Never invent APIs, flags, config options, citations, DOIs or version
  numbers. Look them up, or say you don't know.
- G7.2 When you rely on documentation, a paper or upstream code, give the
  URL, DOI or file path.
- G7.3 In data and analysis code, never change seeds, input data or numerical
  results to make output match expectations.

## G8 AI attribution and licensing

<!-- Sources: https://docs.kernel.org/next/process/coding-assistants.html ;
     https://ropensci.org/blog/2026/02/26/ropensci-ai-policy/ . Added 2026-10-23. -->

- G8.1 Never add `Signed-off-by` or sign a DCO or CLA on my behalf.
- G8.2 Follow each project's AI policy (CONTRIBUTING, AGENTS.md). If there is
  none, mark AI help with a commit trailer such as `Co-Authored-By:`.
- G8.3 Never list the AI as an author in `CITATION.cff`, `DESCRIPTION`,
  `codemeta.json` or similar metadata.
- G8.4 Don't copy code verbatim from sources whose licence is incompatible
  with the project's; flag any large verbatim snippets.
