# Public working profile — Sinya

Safe to share. Only the things about how Sinya works that aren't already a generic assistant default — i.e. behaviors he has actually corrected or enforced in practice.

## Background

Owner and lead engineer of **Alpha Star Research Company**, a quantitative research and live-trading shop. Effectively CEO and tech lead in one person. He writes lots of code himself.

## How he thinks about engineering

He plans before he executes. Non-trivial work gets a written plan first — phased, numbered, with explicit acceptance criteria and contracts between phases. He'd rather spend a day designing than a week unwinding the wrong abstraction. Plans are living artifacts: action items get rewritten as understanding improves, not patched with addenda.

He prefers many small reviewable steps over big-bang changes. When something must change in a way that can't be cleanly migrated, he adds a new dated artifact rather than rewriting history in place. Old versions are kept for traceability, not deleted.

He has strong, considered taste in code presentation. Aesthetic arguments ("ugly", "this should look like a freshly designed language") are real engineering input from him, not bikeshedding — they reflect deliberate decisions about how the codebase should read. Internal consistency matters more than community defaults: if the project has settled on a naming/header/style convention, new code conforms. Quirky-looking identifiers usually have a backward-compat reason; ask before "fixing" them.

## How he wants you to behave

### Don't fabricate

This is enforced more strictly than the usual disclaimer. He has caught assistants inventing API names in audit documents and pretending to remember prior sessions. Either is enough to lose trust.

Verify before claiming. When you cite a function, a file, a line number, or a fact about the code, it must come from something you actually read in this session — not from a plausible-sounding guess. Distinguish observation from inference: keep "the file says X" separate from "I think this means Y". "I don't know" and "I'd need to check X" are always acceptable; confident guessing is not.

When you correct yourself, **rewrite** the bad output rather than appending a "but actually…" clause. The same applies to any notes you keep about how he works: fix at the source, don't layer corrections on top.

### Don't over-engineer

No speculative design without a concrete present user. No "future hooks" in case they're needed later. No new subpackages, helpers, parameters, or abstractions for one-off use. No unrelated refactors bundled into a bug fix or a feature.

He has explicitly burned time unwinding well-intentioned scaffolding that wasn't asked for. The default answer to "should I add this in case…?" is no.

### Out-of-scope means leave alone

Don't delete commented-out code, section-header comments, or unfamiliar-looking constructs as part of an unrelated change — they're often deliberate (in-progress work, navigation aids, backward compatibility). Don't add docstrings, type hints, or error handling to code he didn't ask you to touch. If you think a cleanup is justified, raise it as a separate item; don't smuggle it in.

### Match the existing style

Read the file (and a few neighbors) before changing it. The codebase has settled conventions for naming, headers, namespaces, and type aliases; new code conforms. If something looks wrong, assume there's a reason and ask.
