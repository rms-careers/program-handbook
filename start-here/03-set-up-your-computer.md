# Step 3: Set up your computer

[← Step 2](02-create-your-github-account.md) · **Step 3 of 7** · [Next: Create your first repository →](04-create-your-first-repository.md)

You need two programs: **VS Code** (where you write code) and **Git** (which makes commits). Then you tell Git who you
are and connect it to your GitHub account.

> **Using a college lab computer?** VS Code and Git may already be installed. Do **not** run the
> `git config --global` commands below on a shared computer. Read
> [Using a shared lab computer](07-other-projects-and-team-work.md#using-a-shared-lab-computer) instead.

## 1. Install VS Code

1. Go to [code.visualstudio.com](https://code.visualstudio.com) and download the installer for your system.
2. Run it and accept the defaults. On Windows, also tick **Add "Open with Code" action** for files and folders. It is
   handy later.
3. Open VS Code.

## 2. Install Git

### Windows

1. Go to [git-scm.com/downloads/win](https://git-scm.com/downloads/win) and download the 64-bit installer.
2. Run it. The installer asks many questions. **Keep the default** for every screen except these two:
   - **Choosing the default editor used by Git:** choose **Use Visual Studio Code as Git's default editor**.
   - **Adjusting the name of the initial branch in new repositories:** choose **Override the default branch name** and
     make sure it says `main`.
3. Leave **Git Credential Manager** selected when asked about a credential helper. It handles signing in to GitHub for
   you.
4. Finish the installer, then **close and reopen VS Code**, so it notices that Git is installed.

### macOS

1. Open the **Terminal** app and type `git --version`, then press Enter.
2. If Git is missing, macOS offers to install the **Command Line Developer Tools**. Click **Install** and wait.
3. Install the **GitHub CLI**, which handles signing in to GitHub: download the macOS installer from
   [cli.github.com](https://cli.github.com) and run it.

### Linux (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install git
```

Then install the **GitHub CLI** using the instructions for your distribution at [cli.github.com](https://cli.github.com).

## 3. Open a terminal inside VS Code

A **terminal** is a window where you type commands. In this program you use the one built into VS Code:

- Menu **Terminal → New Terminal** (or press `` Ctrl+` ``: Control and the backtick key, left of `1`).

A panel opens at the bottom of VS Code. That is where you type the commands in this guide. Type a command, then press
**Enter**.

> In this guide, grey boxes like the one below contain commands. Type them exactly (or copy and paste them). Lines
> starting with `#` are comments for you to read, not to type.

## 4. Check that Git works

```bash
git --version
```

You should see something like `git version 2.47.1`. Any version number is fine. If you see
`'git' is not recognized` or `command not found`, see [Troubleshooting](troubleshooting.md#git-is-not-recognized).

## 5. Tell Git who you are

Every commit is labelled with your name and email. Run these three commands, **with your own details**:

```bash
git config --global user.name "Priya Sharma"
git config --global user.email "the-email-you-used-for-github@example.com"
git config --global init.defaultBranch main
```

- Use the **same email address as your GitHub account**. Otherwise your commits will not show on your GitHub profile.
- Want to keep your email private? On GitHub go to **Settings → Emails**, tick **Keep my email addresses private**, and
  use the `...@users.noreply.github.com` address shown there instead.

Check what you set:

```bash
git config --global --list
```

## 6. Connect Git to your GitHub account

Git needs permission to upload to your GitHub account.

- **Windows:** nothing to do now. The first time you upload (in Step 4), a window titled **Connect to GitHub** appears.
  Click **Sign in with your browser**, sign in to GitHub and click **Authorize**. Windows remembers it after that.
- **macOS and Linux:** run this once and answer the questions as shown:

```bash
gh auth login
```

| Question | Answer |
|---|---|
| Where do you use GitHub? | **GitHub.com** |
| What is your preferred protocol for Git operations? | **HTTPS** |
| Authenticate Git with your GitHub credentials? | **Yes** |
| How would you like to authenticate? | **Login with a web browser** |

It shows a one-time code. Press Enter, paste the code in the browser page that opens, and click **Authorize**.

> **GitHub never asks for your password in the terminal.** If a terminal asks for your GitHub password, stop and see
> [Troubleshooting](troubleshooting.md#asked-for-a-password).

## Checklist

- [ ] VS Code opens, and I can open a terminal inside it.
- [ ] `git --version` prints a version number.
- [ ] `git config --global --list` shows my name and my GitHub email.
- [ ] (macOS/Linux) `gh auth login` finished successfully.

[Next: Create your first repository →](04-create-your-first-repository.md)
