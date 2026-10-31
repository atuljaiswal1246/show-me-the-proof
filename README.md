# show-me-the-proof

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)

A Claude Code skill that stops agents from claiming work is done without proof.

## What it does

"It works" is not done. Before reporting any task as complete, the agent must:

* **Run the verification** — execute the command, run the test, or open the page.
* **Capture the output** — copy the exact command result, test exit code, or screenshot.
* **Present the proof** — show the evidence alongside the completion report.
* **No proof, no done** — if it can't be shown, it's not finished.

## Install

```bash
mkdir -p ~/.claude/skills
cp -r show-me-the-proof ~/.claude/skills/show-me-the-proof
```

Load it in your session:

```
/skill show-me-the-proof
```

Or add it to your `CLAUDE.md` so it's active in every session.

## How it works

```
task complete?
    ↓
agent runs verification command / test / opens page
    ↓
agent captures output / screenshot / exit code
    ↓
agent presents proof with completion report
    ↓
you verify the proof, task is done
```

## What counts as proof

| Type | Example |
|------|---------|
| Command output | `git status` clean tree, `curl` returning 200 |
| Test result | `pytest` exit 0, `npm test` all passing |
| Visible result | Screenshot of the page, console with no errors |
| File evidence | `cat file.md` showing expected content, `ls` showing new file |

## Files

| File | Purpose |
|------|---------|
| `SKILL.md` | The skill — the rule, protocol, and proof examples |

## Contributing

Pull requests welcome. Open an issue to discuss changes first.

## License

MIT