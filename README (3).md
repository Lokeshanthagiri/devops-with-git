# Task 4: Build a Version-Controlled DevOps Project with Git

## Objective
Implement a version-controlled project using Git and GitHub with a clear branching strategy, commit conventions, pull requests, and proper documentation.

## Tools Used
- Git
- GitHub
- Terminal/Command line
- Optional: gitignore.io for .gitignore generation

## Folder Structure
```
my-devops-task/
├── README.md
├── execution_logs.txt
├── screenshots/
├── .gitignore
└── src/   # your code/scripts
```

## Step-by-Step Process

### 1. Initialize Git Repository
```bash
git init
git add .
git commit -m "chore: initial project files + README"
```

### 2. Create and Push Branches
```bash
git branch -M main
git remote add origin git@github.com:<username>/<repo>.git
git push -u origin main

git checkout -b dev
git push -u origin dev
```

### 3. Work on Features
```bash
git checkout -b feature/<ticket>-short-desc
# make changes
git add .
git commit -m "feat(feature-name): description"
git push -u origin feature/<ticket>-short-desc
```
Open a Pull Request on GitHub from `feature/...` to `dev`.

### 4. Merge Strategy
- Use Pull Requests for all merges.
- Merge `dev` to `main` after testing/stabilizing.

### 5. Create .gitignore
Example:
```
node_modules/
dist/
.env
__pycache__/
*.pyc
.vscode/
*.log
```

### 6. Tag and Release
```bash
git tag -a v1.0.0 -m "release: v1.0.0"
git push origin v1.0.0
```
Create a GitHub Release from the tag.

## Commit Message Convention
```
<type>(<scope>): <short summary>
```
Types: `feat`, `fix`, `chore`, `docs`, `refactor`.

## Pull Request Template
- **Summary**: What is being changed?
- **Testing**: Steps to test.
- **Checklist**: [ ] Tests run, [ ] Docs updated.

## Submission
- Ensure README.md, `.gitignore`, logs, and screenshots are in the repo.
- Submit the repository link as per instructions.
