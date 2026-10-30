# Step 1: What Git and GitHub are

[← Start here](README.md) · **Step 1 of 7** · [Next: Create your GitHub account →](02-create-your-github-account.md)

## The problem they solve

Imagine writing a program and saving it as `program.py`, then `program-v2.py`, then `program-final.py`, then
`program-final-REALLY.py`. You quickly lose track of what changed and when. If your laptop breaks, everything is gone.
And if two classmates edit the same file, someone's work gets overwritten.

**Git** and **GitHub** solve these problems.

## Git: save points for your code

**Git** is a free program that runs on your computer. It keeps a history of your project as a series of **save points**,
called **commits**.

Think of a video game. You reach a checkpoint and the game saves. If something goes wrong later, you can go back to that
checkpoint. Git does the same for your code:

```text
commit 1             commit 2              commit 3
"Add simple          "Add temperature      "Fix rounding in
 interest program"    converter"            temperature converter"
     ●──────────────────────●───────────────────────●   ← you are here
```

Each commit records **what** changed, **when**, **who** changed it, and a short **message** explaining why.

## GitHub: the online home for your projects

**GitHub** (github.com) is a website that stores copies of Git projects online. When you upload your commits to GitHub:

- your work is **backed up**: a broken laptop no longer means lost work;
- you can **share** it: your tutor, teammates and future employers can see it with a link;
- your teammates can **work with you** on the same project without overwriting each other.

Git is the tool on your computer. GitHub is the website. You use them together.

## The words you need today

| Word | Meaning |
|---|---|
| **Repository** (or **repo**) | A project folder that Git tracks: your files plus their full history. |
| **Commit** | A save point. You choose when to make one and write a message describing it. |
| **Push** | Upload your new commits from your computer to GitHub. |
| **Clone** | Download a repository from GitHub to your computer, the first time. |
| **Template** | A ready-made starting repository that you copy into your own account. |
| **Organisation** | A shared GitHub account owned by a group. RMS Careers' organisation is `rms-careers`. |

More words are in the [Glossary](glossary.md).

## How RMS Careers uses GitHub

The `rms-careers` organisation at [github.com/rms-careers](https://github.com/rms-careers) contains:

| Repository | What it is | What you do with it |
|---|---|---|
| `program-handbook` | This handbook | Read it |
| `template-weekly-labs` | Starter files for your weekly lab repo | Copy it once, in Step 4 |
| More templates over time | Starter files for later projects | Copy them when a project brief tells you to |

**You never upload work to the `rms-careers` organisation.** Everything you build goes in **your own** account. That way:
- your work stays yours after the program ends;
- every project counts towards your GitHub profile, which recruiters look at;
- you can pin your best projects on your profile page.

## Why your repositories are public

Your project repos are **public** by default, which means anyone with the link can see them. This is normal for student
portfolios and is exactly what recruiters want to see. It also means **you must never put passwords, secret keys or
anyone's personal data in a repository**. You will learn how to avoid that in Step 5.

## Check your understanding

Before moving on, you should be able to answer:
1. Which runs on your computer, Git or GitHub?
2. What is a commit?
3. Where does your work go: the `rms-careers` organisation or your own account?

(Answers: Git; a save point with a message; your own account.)

[Next: Create your GitHub account →](02-create-your-github-account.md)
