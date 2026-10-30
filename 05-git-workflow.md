# 5. Git workflow

## Commits

- Commit small, working steps: one idea per commit.
- Write the message as an instruction saying what the commit does: `Add CSV error log`, `Fix fine calculation for
  returns on due date`. Avoid `update`, `changes`, `final`, `final2`.
- Commit at least once every working session. A long, steady history is evidence of your own work.

```bash
git status
git add <files>
git commit -m "Add monthly summary report"
git push
```

## Branches and pull requests (team work)

```bash
git switch -c feature/monthly-report
# ...work and commit...
git push -u origin feature/monthly-report
```

Then open a pull request (PR) on GitHub:
- **Title:** what the PR does.
- **Description:** what changed, how to test it, and a screenshot for UI changes.
- Ask a teammate to review it. **Nobody merges their own PR without a review.**

After merging, update your local `main`:

```bash
git switch main
git pull
```

## Reviewing a teammate's PR

- Read the whole change, and run it if you can.
- Comment on specific lines and explain *why*: "This crashes when the file is empty. Could we check `if not rows`
  first?"
- Be specific and kind; review the code, not the person.
- Approve only when you would be happy to maintain this code yourself.

## Merge conflicts

A conflict means two people changed the same lines. Git marks them like this:

```text
<<<<<<< HEAD
your version
=======
their version
>>>>>>> feature/other-branch
```

Edit the file to the correct final version, delete the markers, then:

```bash
git add <file>
git commit
```

When unsure, ask the teammate who wrote the other version. Never resolve a conflict by deleting their work.
