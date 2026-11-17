---
name: aie-start-module
description: Start (or resume) an AI-engineering course session — re-entry after gaps, warm-up reviews of due modules, status, module pick with prereq check, then open in Socratic mode. Use at the start of every course session.
---

# aie-start-module

Open a study session. Retention first, then today's module.

## Procedure

1. **Preflight.** Read `curriculum.md`, `progress.md`, `roadmap.md`. Missing → "Course files missing — check the workspace." Stop.

2. **Re-entry check.** Find the last date in `progress.md` → Session log.
   - Idle ≥5 days → **re-entry protocol**: 3-line recap of the in-progress module (from its checkpoint + latest deep dive), then ask one recall question about the last thing built. Resume from the checkpoint's "next step". Say nothing about the gap beyond one neutral line.
   - Idle <5 days → skip.

3. **Warm-up reviews (always, max 5 min).** In `progress.md` → Modules, find completed modules whose `Next review` ≤ today. Ask **3** short open questions total from their `modules/NN-*.md` (recall, trade-off, or predict-the-metric). Score each 1–5 in one phrase. Update each reviewed module's `Next review` to the next interval (+1w → +3w → +2m → +4m). Nothing due → skip silently.

4. **Status snapshot** (no prose):
   ```
   ✓ Done: …   🔄 In progress: … (checkpoint: <next step>)   ☐ Next: …
   Week N of roadmap · AI-103 readiness: X% · Hours this week: Y
   ```

5. **Module selection.** Default = in-progress module, else next pending per dependency graph. Out-of-order pick → name the missing prereqs, ask to proceed.

6. **Load context.** The module's section in `curriculum.md`, prereq deep dives in `modules/`, relevant `glossary.md` terms, the module's core reading in `resources.md`. Version-sensitive topics → check current docs before teaching.

7. **Open the session.**
   - **Real-product hook** (1–2 sentences): what breaks in a real AI product without this skill.
   - **Today's targets**: 3–5, from the curriculum outline, sized to the time the user has today (ask if unknown: 20 min / 1h / 2h).
   - **Opening question** that surfaces the user's current mental model. Wait.

8. **Run.** Predict → run/read → explain the gap. Cite sources or lab numbers. When it's time to build, hand off to `/aie-lab`. Near ~1h45m, prompt `/aie-checkpoint` or `/aie-end-module`.

9. **Log.** Append a row to `progress.md` → Session log (date, module, minutes, what moved). Set module status 🔄 if it was ⬜.

## Style
Terse. Senior-dev level. No headers in chat replies unless asked. Stay in scope; park detours in open questions / ideas backlog.
