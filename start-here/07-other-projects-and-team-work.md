# Step 7: Other projects and team work

[← Step 6](06-submit-your-work.md) · **Step 7 of 7** · [Back to Start here](README.md)

Read this in Week 3, when you first work in a team and start projects outside `rms-weekly-labs`.

## Starting a new project

Every project brief tells you which of these two ways to start.

### A. From an RMS template

Same as Step 4: open the template link in the brief → **Use this template** → **Create a new repository** → Owner:
**your username** → the repo name given in the brief → **Public** → **Create repository**. Then clone it.

The brief links to a **version** of the template, for example `.../tree/v1.0`. That is the version your batch uses.

### B. An empty repository

1. On GitHub, click **+** (top right) → **New repository**.
2. **Owner:** your username. **Repository name:** as given in [Repository rules](../03-repository-rules.md).
   **Visibility:** Public. Tick **Add a README file**. Under **Add .gitignore**, choose the language you will use
   (for example **Python** or **Node**).
3. Click **Create repository**, then clone it exactly as in Step 4 Part B.

Clone every project into your `Documents/rms` folder, **next to** `rms-weekly-labs`, never inside it:

```text
Documents/rms/
├── rms-weekly-labs/       ✅
├── campus-marketplace/    ✅
└── mp1-library-manager/   ✅
```

Before cloning, make sure the terminal is in the `rms` folder (`cd ~/Documents/rms`). A repo inside another repo
causes confusing errors.

## Working in a team

In team projects (Week 3 Part B, Week 11, mini projects and the capstone), **one** member creates the repository in
their own account, and the others join it as **collaborators**.

### The owner adds teammates

1. Open the repository → **Settings** → **Collaborators** (left menu).
2. Click **Add people**, type a teammate's GitHub username, and send the invitation.
3. Repeat for each teammate.

### Teammates accept

Each teammate gets an email and a notification on GitHub. Open it and click **Accept invitation** (invitations expire
after 7 days). Then clone the repository with its link, as in Step 4 Part B.

> **Do not fork a team repository.** Commits you make in a fork do not appear on your profile's contribution graph
> unless they are merged back, and your tutor checks each member's commits. Be a collaborator instead.

### How a team works without overwriting each other

Each person works on their own **branch** (a separate line of work) and merges it through a **pull request** that a
teammate reviews. The full workflow, with commands, is in [Git workflow](../05-git-workflow.md). The short version:

```bash
git pull                                  # get everyone's latest work first
git switch -c feature/my-feature          # make your own branch
# ...edit, save, git add, git commit (as in Step 5)...
git push -u origin feature/my-feature     # upload your branch
# then on GitHub: open a pull request and ask a teammate to review it
```

For team projects, each member submits the **same repository link** in the portal and lists **their own** features and
pull request links in **Notes for Reviewer**.

## Using a shared lab computer

College lab computers are shared, so:

1. **Do not run `git config --global`.** Inside your own repository folder, set your details for that repo only:

   ```bash
   git config user.name "Priya Sharma"
   git config user.email "the-email-you-used-for-github@example.com"
   ```

2. **Push before you leave.** Anything only on the lab computer may be gone tomorrow.
3. **Sign out when you finish:**
   - Sign out of github.com in the browser.
   - **Windows:** open **Credential Manager** from the Start menu → **Windows Credentials** → remove every entry that
     starts with `git:https://github.com`.
   - **macOS/Linux with GitHub CLI:** run `gh auth logout`.
4. Optionally, delete your project folder from the lab computer. Your work is safe on GitHub, and you can clone it again
   next time.

## Working on two computers (for example laptop and lab)

GitHub is the meeting point. On whichever computer you sit down at:

```bash
git pull      # always first: get the latest commits from GitHub
# ...work, commit...
git push      # always last: send your commits to GitHub
```

If you forget and both computers have new commits, `git push` is rejected. See
[Troubleshooting](troubleshooting.md#push-rejected).

[Back to Start here](README.md)
