# GitHub for Beginners

*A simple, practical guide to understanding GitHub and using it without making a mess.*

You do not need to become a Git expert to start using GitHub. Learn a few ideas, follow one safe workflow, and build the habit of saving your work regularly.

---

## 1. First, understand Git vs GitHub

They are related, but they are not the same thing:

- **Git** is a tool on your computer that tracks changes to your project. It lets you save checkpoints and compare or restore versions.
- **GitHub** is a website that hosts Git repositories online. It helps you back up code, collaborate with people, review changes, and share projects.

Think of Git as the version-history system and GitHub as the online home for your project.

## 2. The 10 words you should know

| Word | Plain-English meaning |
|---|---|
| **Repository (repo)** | A project folder whose history is tracked by Git. |
| **Commit** | A named checkpoint of your changes. |
| **Branch** | A separate line of work where you can make changes without disturbing another line. |
| **Push** | Send your local commits to GitHub. |
| **Pull** | Bring newer commits from GitHub into your local branch. |
| **Clone** | Download a repository, including its Git history, to your computer. |
| **Fork** | Make your own GitHub copy of someone else's repository. |
| **Pull request (PR)** | Ask for your changes to be reviewed and merged into another branch or repository. |
| **Issue** | A place to report a bug, suggest an improvement, or discuss a task. |
| **README** | The front page of a repository. It explains what the project is and how to use it. |

## 3. Set up GitHub the easy way

### Step 1 — Create your account

Go to [github.com](https://github.com/) and create an account. Use an email address you can access and enable two-factor authentication when you can.

### Step 2 — Install GitHub Desktop

For a beginner, [GitHub Desktop](https://desktop.github.com/) is a friendly way to use Git without memorising commands. Sign in with your GitHub account.

You can use Git from the terminal too, but you do not need to start there.

### Step 3 — Install an editor

[Visual Studio Code](https://code.visualstudio.com/) is a common free editor. You can open a project folder in it, edit files, and use its built-in terminal later.

## 4. Create your first repository

1. Sign in to GitHub.
2. Select **New repository** (or open [github.com/new](https://github.com/new)).
3. Give it a short, clear name, such as `python-practice` or `my-first-project`.
4. Add a one-line description explaining what it does.
5. Choose **Public** if you are happy for anyone to see the code, or **Private** if you want to keep it restricted.
6. Select **Add a README file**.
7. Add a `.gitignore` template if the project language is offered. A `.gitignore` tells Git which generated or private files it should not track.
8. Select **Create repository**.

You now have an online repository. It is fine to start with one file and improve it as you learn.

## 5. Put a project on GitHub

There are two beginner-friendly ways.

### Option A — You already have a project folder on your computer

1. Open GitHub Desktop.
2. Choose **File → Add local repository** if the folder is already a Git repository. If it is not, choose **File → New repository** and select that folder.
3. Give the repository a name and create it if needed.
4. Review the files listed as changed.
5. Write a short summary, such as `Add first Python exercises`.
6. Select **Commit to main**.
7. Select **Publish repository** to put it on GitHub. Choose Public or Private deliberately.

### Option B — The repository already exists on GitHub

1. Open GitHub Desktop.
2. Choose **File → Clone repository**.
3. Select the repository and choose where to save it on your computer.
4. Open the downloaded folder in your code editor.
5. Make a small change and save the file.
6. Return to GitHub Desktop. Review the changed files.
7. Enter a commit summary and select **Commit to main** (or the branch you are using).
8. Select **Push origin** to send the commit to GitHub.

**Remember:** saving a file in your editor does not automatically upload it to GitHub. You must commit the change and then push it.

## 6. The everyday workflow

For a personal project where you are the only person working on it, this simple routine is usually enough:

1. **Pull** — get the latest version before you start, especially if you also edit files on GitHub's website or another computer.
2. **Edit** — make one small, understandable set of changes.
3. **Review** — check the changed files and make sure you did not include anything private or unnecessary.
4. **Commit** — save a checkpoint with a meaningful message.
5. **Push** — upload your commits to GitHub.

A commit is a local checkpoint; a push sends it to the online repository. They are two different actions.

## 7. Branches and pull requests — the basic idea

When you are experimenting or working with other people, avoid making every change directly on the main branch.

A branch is a separate workspace for a change. For example:

- `main` — the stable version of the project.
- `add-login-page` — work for a login-page feature.
- `fix-navbar-mobile` — work to fix the mobile navigation.

A common collaboration flow is:

1. Create a new branch.
2. Make and commit your changes on that branch.
3. Push the branch to GitHub.
4. Open a **pull request** (PR).
5. Explain what changed and how you tested it.
6. Let the changes be reviewed. Fix anything that needs attention.
7. Merge the PR when it is approved and ready.

A PR is a request for review and integration. Opening one does not automatically mean the changes are merged.

## 8. Contributing to someone else's project

A common open-source workflow looks like this:

1. Read the project's README and `CONTRIBUTING` guide.
2. Check its Issues and Discussions to understand what is needed.
3. Look for a suitable issue, but do not assume a label such as `good first issue` guarantees that it is easy or still available.
4. Comment politely before starting if the project asks contributors to claim an issue.
5. **Fork** the repository to your account.
6. Clone your fork to your computer.
7. Create a branch for your change.
8. Make a focused change and run the relevant tests.
9. Push your branch to your fork.
10. Open a pull request to the original project and clearly explain the change.

Always follow that project's own contribution instructions. Different projects have different rules.

## 9. A few useful Git commands

You can do the same basic work in a terminal. Open the terminal in your project folder.

```bash
# Check which files have changed
git status

# Download the latest commits from the remote and integrate them
git pull

# Stage all changes in the current folder
git add .

# Save a checkpoint with a message
git commit -m "Add first project files"

# Upload your commits to GitHub
git push
```

To download a repository for the first time:

```bash
git clone https://github.com/OWNER/REPOSITORY.git
```

Replace `OWNER/REPOSITORY` with the actual account or organisation name and repository name. You can copy the correct URL using the green **Code** button on the repository page.

To create and switch to a new branch:

```bash
git switch -c add-a-feature
```

You do not need to memorise every command today. Learn what each one does before running commands you find online.

## 10. Keep your repository clean

A tidy repository is easier for other people — and your future self — to understand.

### Use a clear structure

A small project might look like this:

```text
my-project/
├── README.md       # What the project does and how to run it
├── .gitignore      # Files Git should leave out
├── src/            # Main source code
├── tests/          # Tests, if the project has them
└── docs/           # Extra documentation, if needed
```

You do not need to create every folder immediately. Add folders when they have a real purpose.

### Write a useful README

A good README should usually answer:

- What does this project do?
- Why did you build it?
- What does someone need before using it?
- How do they install and run it?
- How can they use or test it?
- Are there screenshots or a demo?
- What is planned next?

Keep it honest. Do not claim features that do not work yet.

### Use meaningful commit messages

Good examples:

- `Add input validation to signup form`
- `Fix mobile navigation spacing`
- `Update installation instructions`

Avoid vague messages such as `changes`, `final`, `stuff`, or `upload`.

### Keep changes focused

A commit should represent one understandable piece of work. It is easier to review and undo a focused change than a huge collection of unrelated edits.

## 11. Important safety rules

- **Never upload passwords, API keys, access tokens, private keys, or personal data.** Keep secrets in environment variables or a local `.env` file, and add `.env` to `.gitignore`.
- Do not assume that deleting a secret from the latest version removes it from Git history. If a secret is exposed, revoke or rotate it immediately.
- Use a `.gitignore` appropriate for your language and tools. Common examples include `.env`, `.venv/`, `venv/`, `node_modules/`, `__pycache__/`, and generated build folders.
- Check whether a repository is Public before uploading anything. Public repositories can be viewed by anyone.
- Do not blindly run terminal commands copied from a post or tutorial. Understand what they do first.
- Avoid destructive commands such as `git reset --hard` and `git clean -fd` until you understand their effects. They can discard work.
- Do not force-push to a shared branch unless the project explicitly asks you to and you understand the consequences.

## 12. Common beginner problems

| What you see | What it usually means | What to check |
|---|---|---|
| `nothing to commit` | Git does not see a new change to save. | Save the file, check `git status`, and make sure the file is not ignored. |
| `nothing to push` | There are no local commits waiting to upload. | Check whether you committed the changes. |
| `rejected` when pushing | The remote branch may have commits you do not have locally. | Stop and inspect the message. You may need to pull and resolve a conflict before pushing. |
| A file is missing from GitHub | It may not have been staged, committed, or pushed. | Check `git status`, then commit and push if appropriate. |
| Merge conflict | Two sets of changes overlap and Git needs help choosing the final result. | Open the conflicted file, understand both versions, resolve it, test it, then commit. Do not delete conflict markers without understanding the code. |
| Authentication failed | Git could not verify your account. | Sign in again through GitHub Desktop or follow GitHub's current authentication instructions. Do not paste passwords into a terminal prompt or a random website. |

If something goes wrong, do not keep running random commands. Start with `git status`, read the full error, and make a backup copy of important uncommitted work before attempting a risky repair.

## 13. A simple checklist for every project

- [ ] The repository has a clear name and description.
- [ ] The README explains what the project does and how to run it.
- [ ] The `.gitignore` excludes generated files and local secrets.
- [ ] No passwords, tokens, or private data are committed.
- [ ] Files and folders have understandable names.
- [ ] Commits have meaningful messages.
- [ ] Changes are reviewed before they are pushed.
- [ ] The project has basic instructions for testing, where relevant.

## 14. What should you learn first?

Do not try to learn all of GitHub in one day. A sensible order is:

1. Create a repository and understand its README.
2. Make a small change and commit it.
3. Push the commit to GitHub.
4. Clone the repository to another folder or computer.
5. Create a branch and open a pull request.
6. Learn how forks and issues work when you are ready to contribute to open source.

**Your first goal:** put one small project on GitHub, write a clear README, and make a few meaningful commits. That is enough to build a solid foundation.

---

## Official resources

- [GitHub Docs — Get started](https://docs.github.com/en/get-started)
- [GitHub Skills — Interactive courses](https://skills.github.com/)
- [GitHub Desktop documentation](https://docs.github.com/en/desktop)
- [Git documentation — Book](https://git-scm.com/book/en/v2)
- [GitHub Docs — About pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests)
- [GitHub Docs — About forks](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks)

*Guide last checked: 21 November 2026. GitHub's interface may change; use the official documentation for current button names and account settings.*
