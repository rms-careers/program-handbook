# Step 4: Create your first repository

[← Step 3](03-set-up-your-computer.md) · **Step 4 of 7** · [Next: Save and upload your work →](05-save-and-upload-your-work.md)

You will copy the RMS template into **your own** GitHub account as a new repository called `rms-weekly-labs`, then
download it to your computer.

## Part A: Copy the template on GitHub

1. Sign in to github.com.
2. Open the template: [github.com/rms-careers/template-weekly-labs](https://github.com/rms-careers/template-weekly-labs).
   Near the top it says **Public template**.
3. Click the green **Use this template** button (top right), then **Create a new repository**.
4. Fill in the form:

   | Field | What to choose |
   |---|---|
   | **Include all branches** | Leave **unticked** |
   | **Owner** | **Your username** (it should already be selected) |
   | **Repository name** | `rms-weekly-labs` (exactly, all lowercase) |
   | **Description** | `My weekly labs from the RMS Careers program` |
   | **Visibility** | **Public** |

5. Click **Create repository**.

After a few seconds you land on your new repository at `https://github.com/YOUR-USERNAME/rms-weekly-labs`. Under the
name it says **generated from rms-careers/template-weekly-labs**. That is how you know it is your own copy.

> **Did it say "rms-careers/rms-weekly-labs"?** That cannot happen, because students cannot create repositories in
> the organisation. If the Owner field shows anything other than your username, stop and ask your tutor.

### Add the program topic

On your repository's main page, find **About** on the right and click the **gear icon** next to it. In **Topics**, type
`rms-careers` and press Enter, then click **Save changes**.

Do not add your college name or batch as topics.

## Part B: Download it to your computer (clone)

### 1. Copy the repository link

On your repository page, click the green **<> Code** button, make sure the **HTTPS** tab is selected, and click the
**copy** icon next to the link. It looks like:

```text
https://github.com/YOUR-USERNAME/rms-weekly-labs.git
```

### 2. Choose where your projects will live

Open VS Code and a terminal (**Terminal → New Terminal**). Make a folder for all your program work and move into it:

```bash
cd ~/Documents
mkdir rms
cd rms
```

- `cd` means "change directory", that is, go into a folder. `~/Documents` is your Documents folder.
- `mkdir` means "make directory", that is, create a folder.
- If `mkdir` says the folder already exists, that is fine. Just run `cd rms`.

### 3. Clone

Type `git clone`, a space, then paste the link you copied (right-click in the terminal, or `Ctrl+V`):

```bash
git clone https://github.com/YOUR-USERNAME/rms-weekly-labs.git
```

You should see `Cloning into 'rms-weekly-labs'...` and `done`. Git has created a folder called `rms-weekly-labs`
containing all the files **and** the connection back to GitHub.

### 4. Open the repository in VS Code

1. **File → Open Folder...**
2. Go to `Documents → rms → rms-weekly-labs` and click **Select Folder** (Windows) or **Open** (macOS).
3. If VS Code asks **Do you trust the authors of the files in this folder?**, click **Yes, I trust the authors**.

On the left you now see the files: `README.md`, `LICENSE`, and folders `week-01`, `week-02`, and so on.

> **Always open the `rms-weekly-labs` folder itself**, not the `rms` folder above it. If you open the wrong folder, Git
> commands will say "not a git repository".

## What is in the template

| File or folder | What it is for |
|---|---|
| `README.md` | The front page of your repo. You fill in your name and target role in Step 5. |
| `week-01/`, `week-02/`, ... | One folder per week whose work lives in this repo. Each has a `README.md` checklist for that week. |
| `.gitignore` | Tells Git which files never to upload, such as secret `.env` files. Do not delete it. |
| `.editorconfig` | Keeps spacing consistent. You can ignore it. |
| `LICENSE` | The licence for the starter files. You can keep it. |

Files starting with a dot may be hidden in your file explorer. VS Code shows them.

## Checklist

- [ ] `https://github.com/YOUR-USERNAME/rms-weekly-labs` exists and says "generated from rms-careers/template-weekly-labs".
- [ ] The repository is **Public** and has the `rms-careers` topic.
- [ ] The `rms-weekly-labs` folder is on my computer and open in VS Code.

[Next: Save and upload your work →](05-save-and-upload-your-work.md)
