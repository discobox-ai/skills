# skills

SDLC agent skills used to develop [discobox](https://github.com/discobox-ai/discobox):
triaging and delivering issues, building an agreed change, committing,
verifying, testing, opening pull requests, pushing to main, and orchestrating
many issues across worker discoboxes.

| Skill | What it does |
| --- | --- |
| `commit` | Organize outstanding changes into logical commits |
| `develop` | Build an agreed change and deliver it as a pull request |
| `deliver-issue` | Take one issue from implementation to a merged pull request |
| `triage-issue` | Reproduce, classify, and label one issue |
| `orchestrate-issues` | Run a set of issues across worker discoboxes |
| `verify` | Verify a change at runtime by driving the affected flow |
| `test-fix` | Test a change, then QA it against the running `task dev` loop |
| `open-pr` | Open a pull request and drive its CI green |
| `push-main` | Push to `main` and drive CI green |

This repository is where these skills live: they are no longer kept in, or
synced from, `discobox-ai/discobox`. Change them here, by pull request or a push
to `main`.

They still assume they are working on `discobox-ai/discobox`: its Taskfile and
`task dev` loop, `discobox-ai/discobox` on GitHub, and the skills it keeps for
itself in its own `.agents/skills` — above all `verify-recipes`, whose
`driving-task-dev.md` is what `triage-issue` and `test-fix` read to drive the
`task dev` loop.

## Use

Add this repository as a project skills source so every discobox carries it:

```bash
discobox skills add https://github.com/discobox-ai/skills
```

or for one discobox, `discobox run --skills https://github.com/discobox-ai/skills`.
Skills are linked from the checkout, so an edit made while using one can be
committed and pushed back here.
