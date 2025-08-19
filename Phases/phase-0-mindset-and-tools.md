# Phase 0 — Mindset & Tools (0–2 weeks)

Goal: Set up your environment and adopt a growth mindset for learning.

## Setup

- Install VS Code and essential extensions: GitLens, Prettier, ESLint (if using JS/TS), Python extension (if using Python).
- Install Git and create a GitHub account.
- Install chosen language runtime (Python, Node.js, Java, or .NET SDK).
- Configure your terminal (zsh) and learn basic shell commands.

### Definition
- Setup: The actions and tools you install and configure to write, run, and manage code.

### Discussion
- Spend time getting your environment stable: an editor with useful extensions, Git configured with your name/email, and the language runtime correctly installed. A reliable setup prevents friction when learning and debugging.

### Examples (terminal)
- Configure Git (replace with your name/email):

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

- Initialize a repo, add a file and push to GitHub (after creating the remote):

```bash
git init
echo "print(\"hello\")" > hello.py
git add .
git commit -m "initial commit"
# add remote then push
# git remote add origin git@github.com:you/repo.git
# git push -u origin main
```

- Run a simple script (Python example):

```bash
python3 hello.py
```

## First tasks

- Create a Git repo and push a "hello-world" project.
- Learn to run code from the terminal and debugger in VS Code.
- Learn how to open issues and create simple pull requests on GitHub.

### Definition
- First tasks: Practical, small steps that verify your setup and introduce key workflows (commit, push, PR).

### Discussion
- These tasks are deliberately small but important: they prove that your tools work end-to-end and introduce collaboration basics (issues/PRs) early. Treat them as checks before diving into larger learning goals.

## Mindset

- Embrace incremental learning: break problems down and iterate.
- Learn from errors — write down interesting bugs you fixed.
- Set measurable short-term goals (e.g., finish language tutorial in 2 weeks).

### Definition
- Mindset: The attitudes and habits (patience, curiosity, resilience) that support consistent learning and problem-solving.

### Discussion
- Software engineering is as much about mindset as technical skills. Practice patience, celebrate small wins, reflect on mistakes, and keep a learning journal. Build habits that enable sustained progress.
