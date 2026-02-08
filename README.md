
---

## Git Workflow

This project follows a basic Git workflow commonly used in DevOps teams.

### 1. Repository Initialization
- The repository was initialized locally using `git init`.
- A `.gitignore` file was created to exclude unnecessary files.
- The repository was linked to GitHub as a remote repository.

---

### 2. Branching Strategy
- The `main` branch represents the stable version of the project.
- A separate branch named `experiment` was created to simulate feature development and experimentation.

---

### 3. Working on a Feature Branch
- Placeholder files were added in the `docker`, `k8s`, and `iac` folders.
- Documentation updates were made in the `README.md`.
- Changes were committed with descriptive commit messages.

---

### 4. Simulated Collaboration
- Additional changes were made directly on the `main` branch to simulate another collaborator working in parallel.
- This created a divergence between branches, similar to a real team environment.

---

### 5. Merging and Conflict Resolution
- The `experiment` branch was merged into the `main` branch.
- Any merge conflicts (such as in `README.md`) were resolved manually.
- A merge commit was created to record the integration of changes.

---

### 6. Pull Request Simulation
- A Pull Request (PR) was created on GitHub from `experiment` to `main`.
- The PR was reviewed and merged to simulate a collaborative workflow.
- The updated `main` branch was pulled back to the local repository.

---

### 7. Tagging
- A version tag `v1.0` was created to mark the completion of Milestone 1.
- The tag was pushed to GitHub to represent a release point.

---

## Tools Used
- Visual Studio Code
- Git
- GitHub

---

## Contribution Guidelines
1. Create a new branch for any changes.
2. Make incremental commits with clear messages.
3. Push the branch to GitHub.
4. Open a Pull Request for review.
5. Merge approved changes into `main`.
6. Tag releases when milestones are completed.

