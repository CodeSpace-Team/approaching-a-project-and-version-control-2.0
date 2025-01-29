# Branching and Merging Basics

Branches are one of Git's most powerful features, allowing developers to work on isolated versions of their code without affecting the main project. In this lesson, we'll explore branching and merging fundamentals with clear explanations, examples, and illustrations.

## What Are Branches?

### Definition:

A branch in Git is a lightweight, movable pointer to a commit. Branching allows you to create separate environments for developing, testing, or experimenting with features while keeping the main project stable.

### Illustration:

```plaintext
Main branch history:
A -- B -- C
```

When a new branch is created, it diverges from the main branch:

```plaintext
Main:    A -- B -- C
Feature:          \
                   D
```

## Why Use Branches?

- **Isolated Development:** Safely experiment without affecting the stable codebase.
- **Parallel Workflows:** Multiple team members can work on different features simultaneously.
- **Testing Features:** Test new ideas before integrating them into the main project.
- **Code Review:** Branches make it easier to manage and review changes before merging.

**Example Scenario:**

Imagine you're adding a new navigation bar to your website. Instead of modifying the main code directly, you can create a `feature/navigation-bar` branch, make changes there, and merge it once it's complete and tested.

## Creating a Branch

To create a new branch, use:

```bash
git branch <branch-name>
```

Example:

```bash
git branch feature/navigation-bar
```

Now, you have a branch named `feature/navigation-bar` that points to the same commit as the current branch.

## Switching Between Branches

Switching to a different branch updates your working directory to reflect that branch's state.

**Commands:**

- Using `git checkout`:
  ```bash
  git checkout <branch-name>
  ```
- Using `git switch` (preferred for newer versions of Git):
  ```bash
  git switch <branch-name>
  ```
  **Example:**

Switch to the feature/navigation-bar branch:

```bash
git switch feature/navigation-bar
```

## Merging Branches

Merging integrates changes from one branch into another. Typically, you'll merge a feature branch into the main branch after testing.

**Command:**

```bash
git merge <branch-name>
```

**Example Workflow:**

1. Switch to the main branch:
   ```bash
   git switch main
   ```
2. Merge the feature branch:
   `bash
git merge feature/navigation-bar
`

**Illustration:**

Before merging:

```plaintext
Main:    A -- B -- C
Feature:          \
                   D
```

After merging:

```plaintext
Main:    A -- B -- C -- D
```

## Resolving Merge Conflicts

A merge conflict occurs when Git can't automatically reconcile changes between branches.

**Steps to Resolve:**

1. Attempt the merge:
   ```bash
   git merge <branch-name>
   ```
2. Git will pause the merge and highlight conflicting files. Open the conflicting file to see markers like:
   ```plaintext
   <<<<<<< HEAD
   // Code from the current branch
   =======
   // Code from the branch being merged
   >>>>>>> branch-name
   ```
3. Manually edit the file to resolve the conflict, choosing or combining changes as needed.
4. Mark the conflict as resolved:

```bash
git add <conflicting-file>
```

5. Complete the merge:

```bash
git commit
```

**Example Conflict Resolution:**

If index.html has a conflict:

```plaintext
<<<<<<< HEAD
<h1>Main Branch Heading</h1>
=======
<h1>Feature Branch Heading</h1>
>>>>>>> feature/navigation-bar
```

Resolved version:

```html
<h1>Main Branch Heading</h1>
<h1>Feature Branch Heading</h1>
```

## Activities

### Create a New Branch for a Feature

1. Create a new branch for adding a navigation bar:

   ```bash
   git branch feature/navigation-bar
   git switch feature/navigation-bar
   ```

2. Add the navigation bar code and commit the changes:

   ```bash
   git add .
   git commit -m "Add navigation bar"
   ```

### Merge the Feature Branch

1. Switch to the main branch:

   ```bash
   git switch main
   ```

2. Merge the feature branch:

   ```bash
   git merge feature/navigation-bar
   ```

### Simulate and Resolve a Merge Conflict

1. Create a conflicting situation:
   - On the main branch, edit index.html and commit.
   - Switch to feature/navigation-bar, edit the same section of index.html, and commit.
2. Attempt to merge:

   ```bash
   git merge feature/navigation-bar
   ```

3. Resolve the conflict as outlined in the steps above.
