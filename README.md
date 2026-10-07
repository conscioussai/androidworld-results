# ConscioussAI: a perfect 116/116 on AndroidWorld

**Our phone agent completed every one of the 116 [AndroidWorld](https://github.com/google-research/android_world) tasks, with one attempt per task, inside the benchmark's step limits, using about half the steps allowed.**

AndroidWorld is the open benchmark for AI agents that operate a real Android phone: 116 tasks across 20 everyday apps, from messages, calendars and contacts to notes, expenses, recipes, media and system settings. Every task is graded automatically by AndroidWorld's own evaluator, which checks the phone's actual state when the agent says it is done.

## Highlights

- **116 / 116 tasks completed (100%)**, pass@1, no retries.
- **Efficient:** 1,200 steps used out of 2,349 allowed, about half the step budget.
- **Under the official rules:** official task seed, AndroidWorld's per-task step limits with every app launch counted, and a fresh app state for every task.
- **Fully traceable:** every task's result and every action the agent took are in this repo.

## About ConscioussAI

ConscioussAI builds an AI agent that gets real things done on your phone, in the apps you already use. The agent in this result runs on the same engine as our consumer app.

## Run details

| | |
|---|---|
| **Result** | 116 / 116 (100%), pass@1, one attempt per task |
| **Date** | 29 September 2026 |
| **Agent** | ConscioussAI phone agent (Android app) |
| **Models** | Google Gemini 3.8 Flash, Anthropic Claude Haiku 4.5, Jev |
| **Input** | Screenshot + accessibility tree |
| **Protocol** | Official task seed 30; AndroidWorld's per-task step limits (app launches counted); fresh app state for every task; graded by AndroidWorld's evaluator |
| **Fingerprints** | APK sha256 `3f6bb895dfb74626e37b1c790f0b203f30751dc15a580a903e84b5c3a41cc987`; AndroidWorld commit `e3fea3ccc69787570e282c99573298f1c3019a34` |

## What's in this repo

- `results.csv`: one row per task with whether it passed, the steps used, and AndroidWorld's step budget.
- `trajectories/<task>.csv`: the agent's actions in order. Each row gives the step number, the action, the visible label of the element acted on, and whether the screen changed.

## Verification

A verification kit (APK and run scripts) is available to screened researchers under NDA. Contact: shiven@consciouss.co, manas@consciouss.co
