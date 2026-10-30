# 3. Repository rules

## Where each project lives

Every repo is created in **your own** GitHub account.

| Project | Repo name |
|---|---|
| Weekly Builds (individual work) | `rms-weekly-labs`: one repo, one folder per week |
| Portfolio site (Week 9) | `<your-username>.github.io` (or `portfolio`) |
| Week 10 app | `js-quiz-app` or `js-todo-app` |
| Campus Marketplace (Weeks 12–14) | `campus-marketplace` |
| SAP work (Weeks 20–22) | `sap-kaveri-case` |
| Mini projects | `mp1-<app>`, `mp2-placement-db`, `mp3-<app>`, `mp4-<app>` |
| Team repos (Week 3 Part B, Week 11) | `<team-name>-report-tool`, `<team-name>-api-explorer` |
| Capstone | the product name, e.g. `placetrack` |

## Rules

1. **Public by default.** These repos are your portfolio. If you want to keep a repo private until the due date, add
   your tutor as a collaborator before you submit.
2. **A shared repo belongs to one member; the others are collaborators.** Do not work in forks: commits made in a fork
   do not show on your contribution graph unless they are merged into the original repo. The owner adds teammates in
   **Settings → Collaborators**.
3. **Add the topic `rms-careers`** to each repo (the gear icon next to "About"). Do **not** add your college name or
   batch as a topic.
4. **Never commit secrets.** No passwords, API keys, tokens or `.env` files. Commit a `.env.example` with the variable
   names and fake values instead. If you commit a secret by accident, tell your tutor and **rotate** it (create a new
   one and delete the old one). Deleting the commit is not enough, because the secret stays in the history.
5. **Never commit real personal data.** Use synthetic data (for example, generated with Faker) or properly anonymised
   public datasets.
6. **Keep history honest.** Write meaningful commit messages, never one "upload files" commit, and never force-push over
   teammates' work.
