# Step 5: Save and upload your work

[← Step 4](04-create-your-first-repository.md) · **Step 5 of 7** · [Next: Submit your work →](06-submit-your-work.md)

This is the loop you will repeat for the whole program:

```text
 ① edit files ─▶ ② save (Ctrl+S) ─▶ ③ git status ─▶ ④ git add ─▶ ⑤ git commit ─▶ ⑥ git push ─▶ ⑦ check on GitHub
      ▲                                                                                              │
      └──────────────────────────────────────── keep working ◀──────────────────────────────────────┘
```

You will practise it now by filling in your README and adding your first Week 1 program.

## Your first commit: the README

### ① Edit

In VS Code, click `README.md` (the one at the top level, not inside a week folder). Replace the example details with
your own: your name, target role, backup role and GitHub link. Then delete the two lines at the top that start with
`<!--` (they are notes for you and never show on GitHub).

### ② Save

Press **Ctrl+S** (Windows/Linux) or **Cmd+S** (macOS).

> **Git only sees saved files.** A white dot on a file's tab in VS Code means it is not saved yet.

### ③ See what changed

In the VS Code terminal:

```bash
git status
```

Git lists `README.md` under **Changes not staged for commit** (often in red). That means: "this file changed, but it
is not part of a save point yet."

### ④ Choose what goes into the commit

```bash
git add README.md
```

Run `git status` again: `README.md` is now under **Changes to be committed** (often in green). This is called
**staging**: you are choosing what goes into the next save point.

To stage **every** changed file at once, use `git add .` (with a dot). Always run `git status` first so you know what
you are adding.

### ⑤ Make the commit

```bash
git commit -m "Add my details to README"
```

`-m` is followed by the **commit message**, in quotes. A good message says what the commit does:

| Good | Not useful |
|---|---|
| `Add simple interest program` | `update` |
| `Fix rounding in temperature converter` | `changes` |
| `Add sample outputs to week-01 README` | `final` / `final2` |

### ⑥ Upload to GitHub

```bash
git push
```

- **First time on Windows:** the **Connect to GitHub** window appears. Click **Sign in with your browser** and approve
  it (see Step 3).
- You should see lines ending with `main -> main`. That means the upload worked.

### ⑦ Check on GitHub

Open `https://github.com/YOUR-USERNAME/rms-weekly-labs` in your browser and refresh. Your README now shows your
details, and near the top you see your commit message and "1 minute ago".

**You have made and uploaded your first commit.**

## Your second commit: a Week 1 program

1. In VS Code's file list, right-click the `week-01` folder → **New File...** → name it `simple_interest.py`.
2. Type a small program:

   ```python
   principal = float(input("Principal (Rs): "))
   rate = float(input("Rate (% per year): "))
   years = float(input("Time (years): "))

   interest = principal * rate * years / 100
   print(f"Simple interest: Rs {interest:.2f}")
   ```

3. Save it (**Ctrl+S**) and run it in the terminal to check it works:

   ```bash
   python week-01/simple_interest.py
   ```

   (On macOS/Linux use `python3` if `python` is not found.)

4. Commit and push it:

   ```bash
   git status
   git add week-01/simple_interest.py
   git commit -m "Add simple interest program"
   git push
   ```

5. Refresh GitHub and open the `week-01` folder. Your program is there.

## Habits that keep you out of trouble

- **Commit small and often:** one program or one fix per commit. Your Week 1 build asks for at least 5 meaningful
  commits, and a steady history shows your tutor (and recruiters) that the work is yours.
- **Push at the end of every session**, so your work is backed up.
- **Run `git status` before `git add`**, so you never upload something by accident.
- **Never commit secrets:** no passwords, API keys or `.env` files. The template's `.gitignore` already blocks `.env`
  files, so leave it in place.
- **Never commit real personal data** about anyone, including yourself (phone numbers, addresses, marks of real people).
- **Did you edit a file directly on the GitHub website?** Then run `git pull` on your computer before you continue,
  so both copies match. See [Troubleshooting](troubleshooting.md#push-rejected).

## Cheat sheet

| I want to... | Command |
|---|---|
| See what changed | `git status` |
| See exactly which lines changed | `git diff` |
| Stage one file | `git add path/to/file` |
| Stage everything that changed | `git add .` |
| Make a commit | `git commit -m "Describe the change"` |
| Upload commits to GitHub | `git push` |
| Download changes from GitHub | `git pull` |
| See the history | `git log --oneline` |

Press `q` to leave `git log` or `git diff` if the output fills the screen.

[Next: Submit your work →](06-submit-your-work.md)
