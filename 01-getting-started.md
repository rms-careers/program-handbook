# 1. Getting started

## Accounts

| Account | Needed by | Notes |
|---|---|---|
| GitHub | Week 1 | See "Choosing your GitHub username" below. |
| LeetCode and HackerRank | Week 2 | Free tiers are enough. |
| LinkedIn | Week 11 | Built step by step in the career stream. |
| Hosting (Vercel or Netlify, Render, Neon or Supabase) | Week 15 | Free tiers. Check current limits when you sign up. |
| Google account (for Colab) | Week 16 | |
| Naukri | Week 18 | |

You never need to enter payment details for any program activity. The LLM API used in Week 19 is provided by your tutor.

## Tools

| Tool | Needed by |
|---|---|
| VS Code with the Python, ESLint, Prettier and GitLens extensions | Week 1 |
| Python 3.12 or later (with pip and venv) | Week 1 |
| Git | Week 1 |
| PostgreSQL with pgAdmin or DBeaver | Week 5 |
| MongoDB Community + Compass, or a MongoDB Atlas free cluster | Week 8 |
| Node.js LTS with npm | Week 10 |
| Postman or Thunder Client | Week 14 |

Check each install from a terminal:

```bash
git --version
python --version
node --version
```

## Choosing your GitHub username

Recruiters will see this name on your resume, so:

- use your real name or a close variation (`priya-sharma`, `psharma-dev`), not a nickname;
- avoid birth years, college roll numbers and words like "coder" or "hacker";
- if you already have an account with an unprofessional name, you can rename it in **Settings → Account**. Old links
  redirect for a while, but update them everywhere.

Then:
1. Add a profile photo and your name in **Settings → Public profile**.
2. Turn on two-factor authentication (**Settings → Password and authentication**). It protects your portfolio.
3. Add your GitHub profile URL to your RMS student profile, so tutors can find your work.

## Configure Git once

```bash
git config --global user.name "Your Name"
git config --global user.email "the-email-on-your-github-account@example.com"
git config --global init.defaultBranch main
```

Use the email address attached to your GitHub account (or GitHub's private `noreply` address). Otherwise your commits
will not appear on your contribution graph.
