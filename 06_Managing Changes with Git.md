# Managing Changes with Git

## Learning Objectives

By the end of this lesson, students will:

1. Understand the importance of frequent and meaningful commits.
2. Learn the Git workflow: staging, committing, and viewing changes.
3. Use git log to review commit history.
4. Undo changes, fix mistakes, and restore files with Git commands.

## Making Commits

### The Importance of Committing Changes Frequently

- Frequent commits make it easier to track progress and isolate bugs.
- Each commit acts as a snapshot of your project at a specific moment in time.
- Best practice: commit after completing a logical unit of work, such as - implementing a feature or fixing a bug.

### Writing Meaningful Commit Messages

Good commit messages make it easy to understand changes when revisiting the history.

- Good message example:
  ```
  Add login functionality with form validation
  ```
- Bad message example:
  ```scss
  Fixed stuff
  ```

### Tips for Writing Good Commit Messages

1. Use the imperative mood (e.g., "Fix bug," not "Fixed bug").
2. Be concise but descriptive.
3. Include context if needed, e.g., referencing an issue or feature.

## The Git Workflow

### Stage Changes with `git add`

- Staging allows you to select which changes to include in the next commit.
- Add specific files:
  ```bash
  git add filename
  ```
- Stage all changes:
  ```bash
  git add .
  ```

### Commit Changes with git commit

- Commit changes with a message:
  ```bash
  git commit -m "Your commit message"
  ```
- Use the editor for detailed messages:
  ```bash
  git commit
  ```

## Viewing Commit History

### Using `git log`

- View the history of commits:
  ```bash
  git log
  ```
- Understand the output:
  - **Commit hash:** A unique identifier for each commit.
  - **Author:** Who made the changes.
  - **Date:** When the changes were committed.
  - **Message:** The description of the changes.

### Customising the Log Output

- Show one-line summaries:
  ```bash
  git log --oneline
  ```
- Display changes in a graph view:
  ```bash
  git log --graph --oneline
  ```

## Undoing Changes and Fixing Mistakes

### Undoing Uncommitted Changes

- Discard changes in the working directory:
  ```bash
  git restore filename
  ```
- Unstage changes from the staging area:
  ```bash
  git reset filename
  ```

### Reverting a Commit

- **Why revert a commit?**

  Reverting creates a new commit that undoes the changes, preserving the history.

- **How to revert a commit:**
  ```bash
  git revert commit-hash
  ```
- Reverting merges conflict-free changes automatically, but conflicts may require manual resolution.

## Restoring Previous Versions of Files

### Restoring a File from a Specific Commit

1. Use `git checkout` (deprecated but commonly used):
   ```bash
   git checkout commit-hash -- filename
   ```
2. Alternatively, use `git restore`:
   ```bash
    git restore --source=commit-hash filename
   ```

## Activities

### Making and Viewing Commits

1. Create multiple changes in a project (e.g., editing files).
2. Stage and commit each change with meaningful messages.
3. Use `git log` and `git log --oneline` to review the commit history.

### Undoing and Reverting Changes

1. Edit a file and stage it:
   ```bash
   git add filename
   ```
2. Unstage the file using git reset:
   ```bash
   git reset filename
   ```
3. Discard changes to the file using git restore:
   ```bash
   git restore filename
   ```
4. Commit a change, then revert it:
   ```bash
   git revert commit-hash
   ```

### Restoring Files

1. Modify or delete a file in the repository.
2. Restore the file from a previous commit using `git restore`.

## Key Takeaways

1. Commit frequently with meaningful messages to maintain a clear project history.
2. Use the Git workflow (`git add, git commit,` and `git log`) to manage changes.
3. Undo mistakes with `git restore` or `git reset` for uncommitted changes.
4. Revert commits to undo changes without losing history.
5. Restore files from previous commits to recover lost or overwritten work.
