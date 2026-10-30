# Troubleshooting

[← Start here](README.md)

Find the message you see (or something close to it) and follow the fix. If nothing here helps, ask your tutor and
include **the command you ran** and **the full message**. A screenshot of the terminal is ideal.

## Git is not recognized

> `'git' is not recognized as an internal or external command` / `git: command not found`

Git is not installed, or VS Code was open while you installed it.
1. Close **all** VS Code windows and open VS Code again.
2. Run `git --version` again.
3. Still failing? Reinstall Git ([Step 3](03-set-up-your-computer.md#2-install-git)) and restart your computer.

## Not a git repository

> `fatal: not a git repository (or any of the parent directories): .git`

Your terminal is not inside a repository folder. Either:
- open the repository folder itself in VS Code (**File → Open Folder** → `rms-weekly-labs`) and open a new terminal; or
- move into it: `cd ~/Documents/rms/rms-weekly-labs`

## Please tell me who you are

> `Author identity unknown` / `Please tell me who you are`

Git does not know your name and email yet. Run the `git config` commands from
[Step 3 §5](03-set-up-your-computer.md#5-tell-git-who-you-are) (on a lab computer, the repo-only version in
[Step 7](07-other-projects-and-team-work.md#using-a-shared-lab-computer)), then run your `git commit` again.

## Nothing to commit

> `nothing to commit, working tree clean`

Git sees no changes. Usually you **did not save** the file. Press **Ctrl+S** in VS Code (a white dot on the tab means
unsaved), then run `git status` again.

## Nothing added to commit

> `no changes added to commit (use "git add" and/or "git commit -a")`

You changed files but did not stage them. Run `git add <file>` (or `git add .`), then commit.

## Push rejected

> `! [rejected] main -> main (fetch first)` / `Updates were rejected because the remote contains work that you do not have locally`

GitHub has commits that your computer does not: you edited on the GitHub website, pushed from another computer, or a
teammate pushed. Get them first, then push:

```bash
git pull
git push
```

If `git pull` opens an editor asking for a merge message, save and close it (in VS Code, close the tab). If it reports a
**conflict**, see [Merge conflicts](../05-git-workflow.md#merge-conflicts) or ask your tutor. **Never use
`git push --force`** to get around this: it deletes the other commits.

## Asked for a password

> `Username for 'https://github.com':` / `Password for ...`
> or `remote: Support for password authentication was removed`

GitHub does not accept your account password in the terminal.
- **Windows:** Git Credential Manager should have opened a sign-in window. Reinstall Git with the default
  **Git Credential Manager** option ([Step 3](03-set-up-your-computer.md#windows)) and try again.
- **macOS/Linux:** run `gh auth login` ([Step 3 §6](03-set-up-your-computer.md#6-connect-git-to-your-github-account)),
  then try again.

## Permission denied or repository not found

> `remote: Permission to X/Y.git denied` / `fatal: repository '...' not found` / `error: 403`

- You may be signed in as a **different GitHub account** (common on shared computers). On Windows, remove the
  `git:https://github.com` entries in **Credential Manager** and push again to sign in fresh. On macOS/Linux run
  `gh auth status` to see which account is active.
- For a team repo: has the owner added you as a collaborator, and did you **accept** the invitation?
- Check the repository link for typos: `git remote -v` shows it.

## I cloned the template instead of my own copy

`git remote -v` shows `rms-careers/template-weekly-labs`. You cannot push there, and you should not. Delete that folder,
then clone **your** repository (`https://github.com/YOUR-USERNAME/rms-weekly-labs.git`) as in
[Step 4 Part B](04-create-your-first-repository.md#part-b-download-it-to-your-computer-clone).

## A repository inside a repository

VS Code shows strange extra changes, or `git status` lists a whole project folder as one item. You cloned a project
**inside** another project's folder. Move the inner folder out next to the outer one (see
[Step 7](07-other-projects-and-team-work.md#starting-a-new-project)) and ask your tutor if it is already committed.

## LF will be replaced by CRLF

> `warning: in the working copy of 'file', LF will be replaced by CRLF`

A harmless warning on Windows about line endings. You can ignore it.

## I committed a secret (password, API key, .env file)

1. **Tell your tutor straight away.**
2. **Make the secret useless:** create a new key or password with the service and delete the old one ("rotating" it).
   Deleting the file is not enough: it stays in the Git history, and public repos are scanned by bots within minutes.
3. Then remove the file and stop it coming back:

   ```bash
   git rm --cached .env
   git commit -m "Stop tracking .env"
   git push
   ```

## I'm stuck in a strange screen after git log or git diff

Press `q` to quit.

## I'm stuck in an editor after git commit or git pull

You ran `git commit` without `-m`, or Git needs a merge message.
- In VS Code: type a message at the top if the file is empty, save, then close the tab.
- In a terminal editor called Vim (`~` symbols down the left side): press `Esc`, type `:wq` and press Enter.

[← Start here](README.md)
