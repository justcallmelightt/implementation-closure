[English](README.md) | [한국어](README.ko.md)

# Implementation Closure

Implementation Closure is a focused [Agent Skill](SKILL.md) for finishing a feature or bug fix when the reported behavior spans several states, has failed before, or cannot yet be called complete with confidence.

## Use it in a project

Install this directory as `implementation-closure` in your agent's Skills location. For Codex, the local path is `~/.codex/skills/implementation-closure/SKILL.md`. Then ask the agent to finish or repair a concrete implementation; you can also invoke `$implementation-closure` explicitly. The Skill applies to implementation work, not standalone reviews or status questions.

## Designed to close the implementation gap

The Skill asks the agent to establish expected versus observed behavior, inspect the relevant path, make a scoped fix, and recheck both the original failing case and a nearby state or boundary. Its final report separates direct observation, automated checks, and unverified behavior. It does not authorize deployment, pushing, or unrelated changes.

For example, a rolling score that shows `0` but clips `1` and disappears at `2` should be checked at `0 → 1 → 2`, including the alignment of a denominator such as `/ 6`. A passing source-level test alone is not visual proof of that interaction. This is a representative case, not evidence that the Skill already improves outcomes.

## Evaluate it

Compare similar implementation requests with and without the Skill, keeping the model and environment comparable. Record whether the original failure and adjacent state were verified, whether the user had to request another fix, and any extra tool or token cost. A lower re-request rate has not yet been established.
