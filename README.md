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

These were moved verbatim from `discobox-ai/discobox` and still assume that
repository (its Taskfile, `task dev` loop, `verify-recipes` skill, and
`discobox-ai/discobox` on GitHub).

## Use

Add this repository as a project skills source so every discobox carries it:

```bash
discobox skills add https://github.com/discobox-ai/skills
```

or for one discobox, `discobox new --skills https://github.com/discobox-ai/skills`.
Skills are linked from the checkout, so an edit made while using one can be
committed and pushed back here.
