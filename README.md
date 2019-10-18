## 6.1 Github Cheat Sheet

### Getting Started

[The Real Cheat Sheet from Github](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)

`git init` — Initializes current directory as a git repository.
Question: What do we mean by a "local" directory?

### Seeing What's Going On

`git status` - shows status, including staged changes, unstaged changes, and untracked files.
Question: What is an untracked file?

`git diff` - shows unstaged changes in tracked files.

### Creating Commits
`git add` - stages changes to be committed.
 - `“.”` adds all changes in the current directory.
 - `“-p”` looks through the diff to stage changes by "hunk"

`git commit` - creates a commit for all staged changes
 - `“-m”` adds a message in quotes right after (Bonus: we avoid using the VI editor).
 - `“-a”` adds all changes **in tracked files**.
 - `“—amend”` allows us to add staged changes to the previous commit.

### Adjusting Your Changes

`git checkout` - does many things!
- will remove your changes to a tracked file
- `"-b" [branch-name]` will let you change to a new branch 

`git reset` - does many things!
 - will reset staged commits to be unstaged.
 - lets us revert changes from previous commits.
 - be careful!
 
 `git clean` - removes untracked files from repo.
 - be SUPER careful.

### Remote Repositories

`git push` - pushes your branch to a remote repo.

`git pull` - pulls changes from a remote repo to your branch.

`git remote` - references to "non-local" locations for our repo.
 - `"add”` add a new remote.
 - `"-v”` to see locations.
 
 ### Collaboration
 
 `git branch` - shows you which branch you are working on.

 `git checkout -b [branch-name]` lets you create a new branch (as shown above).
 - before creating a new branch, make sure to `git pull` into the `master` branch to make sure you have all remote changes before starting work on your new branch.
 - when you create a new branch, always **(ALWAYS)** make sure you are branching from `master` (do not checkout to a new working branch from another working branch).
 - Note: if you use `git checkout [branch-name]` (without the `-b` option) you can switch between already-existing branches in your local repository.



### QUESTIONS:

The Eternal Question: When should you commit?

What **should not happen** when another developer uses/compiles the code that you've committed?

How can you link your local git repository to github?

Why should you branch from `master`?

What is HEAD? http://researchhubs.com/post/computing/git/what-is-HEAD-in-git.html
