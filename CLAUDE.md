<!-- KEEL:BEGIN — v1.11.0 do not remove: binds every AI/session in this repo to the Keel workflow -->
# Keel protocol (mandatory for ANY assistant working in this repository)

This project is governed by the Keel workflow. Before reading code or changing ANYTHING:

1. Read the FULL Keel `SKILL.md` FIRST, before anything else in this repository —
   from the installed `keel` skill if present, otherwise from the embedded copy
   at `.claude/skills/keel/SKILL.md` — and follow it literally, starting with its
   session-start update check. Remembering the protocol from an earlier chat, or
   having this lock in context, does NOT count as having read it: a session that
   works without having read SKILL.md in this session is out of protocol. If the
   update check installs a newer Keel, re-read the new `SKILL.md` and run its
   post-update reconciliation (defined in Keel's `references/project-state.md`)
   BEFORE normal work continues, so this project is brought up to date with
   everything the new version requires — new files or directories, new
   project-card lines, this very lock block, questions never asked here.
2. Then read `docs/PROGRESS.md` (project card, current position, next action),
   `docs/decisions.md` (decisions are NEVER re-opened on your initiative), and
   `docs/lessons-learned.md` (recorded mistakes are never repeated), plus the
   phase reference SKILL.md names for the current phase. If the project card's
   `Keel baseline:` is older than the running Keel (or missing), offer the
   post-update reconciliation before continuing.
3. Follow the recorded specs and design exactly: no reinterpretation, no silent
   deviation, no "improving" recorded decisions. Anything undefined → ask the user.
   Design gaps → Design Request (Keel Phase 4).
4. Update `docs/PROGRESS.md` and `docs/decisions.md` at the moment of every change.
   Commit at passed test points — never without first checking the staged files for
   confidential data (secrets, credentials, private keys, tokens, real personal or
   customer data). A finding STOPS the commit: warn the user file by file that
   pushing it is a serious security risk, and exclude it via `.gitignore` (already
   tracked: untrack it too; ever pushed: purge history AND rotate the credential)
   before committing anything. If ending mid-work, produce the continuation prompt
   from `.claude/skills/keel/references/project-state.md`.
5. Work with execution discipline, whatever model or environment is running:
   - Batch independent tool calls in ONE parallel block; never run sequentially what
     does not depend on a previous result.
   - Delegate broad searches/scans to a subagent when the environment provides them;
     bring back conclusions, never file dumps — the main context stays clean.
   - Do not narrate between tool calls ("now I will…"); accumulate findings and
     report once, at the end of the work block.
   - Locate before reading: search/grep first, then read only the relevant fragment.
     Never read whole files or directories "for context".
   - Edit surgically (exact-match edits on the changed lines); never rewrite a whole
     file to change one part.
   - Batch clarifying questions at the START of a work block; close every work block
     with an explicit verification step (diff, test, or re-read) before calling it
     done.

This block itself can be outdated: the version stamp on the `KEEL:BEGIN`
delimiter names the Keel that last wrote it. If that stamp differs from the
running Keel version (or is missing), refresh this whole block from the
canonical copy in Keel's `references/project-state.md` ("Portability") —
between the delimiters only, with the user's OK, restamped with the running
version. The stamp alone decides; no content comparison is needed.

If neither the skill nor the embedded copy is available: STOP and tell the user to
install Keel (or restore `.claude/skills/keel/`) before continuing.
<!-- KEEL:END -->
