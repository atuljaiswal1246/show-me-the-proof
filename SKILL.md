---
name: show-me-the-proof
description: Never claim a task is done without evidence — command output, test result, or screenshot.
metadata:
  source: owner, 2026-10-31
  verified: false
---

# show-me-the-proof

## Core rule

Never say a task is finished without proof. A claim of "done" is not evidence — only command output, a passing test, or a visible result is.

## Protocol

Before reporting any task as complete:

1. **Run the verification.** Execute the command, run the test, or open the page that proves the work works.
2. **Capture the output.** Copy the exact command output, test result, or screenshot.
3. **Present the proof.** Show the evidence alongside your completion report.
4. **No proof, no done.** If you can't show it, it's not done.

## What counts as proof

| Type | Example |
|------|---------|
| Command output | `git status` showing clean tree, `python app.py` returning 200 |
| Test result | `pytest` exit code 0, `npm test` all passing |
| Visible result | Screenshot of the page, browser console showing no errors |
| File evidence | `cat file.md` showing expected content, `ls` showing created file |

## Gate

"It works" without proof is not done. If you claim completion without showing the evidence, stop and produce it.

## Example

```
Task: add dark-mode toggle
Proof:
$ git status
On branch main
nothing to commit, working tree clean

$ curl -I http://localhost:3000
HTTP/1.1 200 OK

Screenshot: header shows dark-mode toggle in top-right
```

Do not say "done" until you can show this.