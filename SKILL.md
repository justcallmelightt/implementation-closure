---
name: implementation-closure
description: Finish and verify a requested feature or bug fix when behavior spans multiple states, previously failed, or completion is uncertain. Use for implementation and regression follow-ups, not standalone reviews or status questions.
---

# Implementation closure

Close the gap between changed code and the user's requested behavior.

1. Capture the specific expected behavior and observed failure from the user's report. For an implementation request, identify a reproducible acceptance case before changing code; for a reported bug, reproduce it when the environment permits. Do not treat a screenshot or a passing unit test alone as proof of the whole interaction.
2. Follow the failing path through the smallest relevant code and state transitions. Distinguish the cause from a visual symptom; preserve unrelated work and the user's chosen design.
3. Make the smallest coherent fix within the authorized scope. When the failure reveals several independent issues, fix those needed for the requested outcome and report any remainder.
4. Recheck the original failing case and at least one meaningful neighboring state or boundary (for example, the state before/after a counter change, a second viewport, or an interrupted interaction). Select checks based on the actual failure; do not run a generic test battery for its own sake.
5. Report what was directly observed, what was covered only by automated checks, and what could not be verified. Claim completion only when the requested behavior is confirmed. If blocked by missing access or input, stop at the boundary and state the precise next action needed.

Do not infer permission to deploy, push, change unrelated files, or contact outside systems. This skill does not replace task-specific skills; use one when its specialized procedure is relevant.
