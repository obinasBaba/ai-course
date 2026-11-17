---
name: aie-checkpoint
description: Save mid-module state for the AI-engineering course — what is done, the exact next step / failing test, open questions — so the next session (even weeks later) resumes in under 5 minutes. Use whenever a session ends before the module is finished.
---

# aie-checkpoint

Capture state, not knowledge. Two minutes, no teaching.

## Procedure

1. Identify the in-progress module from `progress.md`.
2. Ask the user (one message, three short prompts):
   - "What did you finish today?"
   - "What's the very next step?" (prefer a concrete failing test name or file)
   - "Anything confusing?"
3. Check the labs repo state yourself: `git -C labs status --short` and the last commit SHA; run `uv run pytest -q` in the lab folder if one exists and note the first failing test.
4. Overwrite `progress.md` → **Checkpoint** section:
   ```
   Module: <NN name> · Date: <today> · Labs SHA: <sha or "uncommitted">
   Done: <bullets>
   Next step: <one concrete action / failing test>
   Confusions: <bullets or "none">
   Hint level reached: <L0–L3 on current step>
   ```
5. Append the Session log row (date, module, minutes, what moved).
6. Copy confusions to Open questions if they aren't resolved.
7. One-line close: "Saved. Next time: <next step>." Stop.
