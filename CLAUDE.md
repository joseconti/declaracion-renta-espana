<!-- KEEL:BEGIN — do not remove: binds every AI/session in this repo to the Keel workflow -->
# Keel protocol (mandatory for ANY assistant working in this repository)

This project is governed by the Keel workflow. Before reading code or changing ANYTHING:

1. Read `docs/PROGRESS.md` (project card, current position, next action), then
   `docs/decisions.md` (decisions are NEVER re-opened on your initiative), then
   `docs/lessons-learned.md` (recorded mistakes are never repeated).
2. If the `keel` skill is installed in this environment, it governs. If it is NOT,
   read the embedded copy at `.claude/skills/keel/SKILL.md` plus the phase reference
   it names for the current phase, and follow it literally.
3. Follow the recorded specs and design exactly: no reinterpretation, no silent
   deviation, no "improving" recorded decisions. Anything undefined → ask the user.
   Design gaps → Design Request (Keel Phase 4).
4. Update `docs/PROGRESS.md` and `docs/decisions.md` at the moment of every change.
   Commit at passed test points. If ending mid-work, produce the continuation prompt
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

If neither the skill nor the embedded copy is available: STOP and tell the user to
install Keel (or restore `.claude/skills/keel/`) before continuing.
<!-- KEEL:END -->
