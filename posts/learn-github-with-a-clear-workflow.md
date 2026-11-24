# Learn GitHub by Following a Workflow, Not Memorising Commands

Git and GitHub can feel complicated when you try to learn every command at once. A better starting point is to understand the small workflow behind most everyday changes.

The goal is not to type commands quickly. It is to know what will change, why you are changing it, and how to check the result.

## 1. Start with the outcome

Before editing a project, write down what you want to be different.

For example:

- Add one feature.
- Fix one bug.
- Improve one section of documentation.

A clear, small outcome makes it easier to review your work and notice when something unrelated changes.

## 2. Inspect before you change anything

Start by understanding the current state:

```bash
git status
git branch --show-current
git log -5 --oneline
```

These commands help answer three useful questions:

- Are there uncommitted changes?
- Which branch am I working on?
- What are the latest saved checkpoints?

If you do not understand the current state, pause before making changes.

## 3. Make one focused change

Avoid mixing unrelated edits into one commit. A focused change is easier to understand, test, review, and undo.

After editing, inspect the difference:

```bash
git diff
git status
```

Read the diff instead of assuming that only the intended lines changed.

## 4. Save a meaningful checkpoint

When the change is ready, stage only the files that belong to it:

```bash
git add README.md
git diff --cached
git commit -m "Improve setup instructions"
```

The filename and commit message above are examples; use the files and message that match your actual change.

A commit records a checkpoint locally. It does not automatically publish that checkpoint to GitHub.

## 5. Push only after reviewing

Before publishing, check the branch and the commits you are about to send. Then push:

```bash
git push
```

If Git reports a rejection or conflict, read the complete message and inspect the repository state. Do not respond by repeatedly running random commands.

## 6. Treat risky commands differently

Some commands can discard work or rewrite shared history. Do not run commands such as `git reset --hard`, `git clean -fd`, or force-push commands just because a tutorial says they are convenient.

First understand what they affect. Keep a backup of important uncommitted work before attempting a risky repair.

Also keep passwords, API keys, tokens, and private data out of commits. Check the files being staged, especially before pushing to a public repository.

## A simple habit to remember

**Define → Inspect → Change → Review → Commit → Push → Verify**

You do not need to master all of Git today. Learn this loop, practise it on a small project, and build confidence through changes you can explain and verify.

The most useful Git skill is not memorising commands. It is developing the habit of checking the state of your work before and after each meaningful action.
