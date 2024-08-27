---
title: "Git Commands Cheat Sheet"
seoTitle: "Mastering Git: The Ultimate Cheat Sheet for Developers and Programmers"
seoDescription: "Optimize your development workflow with our essential Git Commands Cheat Sheet, covering everything from the basics to advanced techniques."
datePublished: Thu Nov 02 2023 08:12:25 GMT+0000 (Coordinated Universal Time)
cuid: clogws7tz000109k09cn49ven
slug: git-commands-cheat-sheet
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698912700112/ceb51062-a550-42db-9fbe-7de2e1159cf4.png
tags: development, version-control, git, coding, tech-skills

---

## Git Vocabulary

1. **Bare Repository**
    
    * A repository that doesn’t have a working directory.
        
2. **Branch**
    
    * An active area of development in Git. The newest commit displays the end of the branch.
        
3. **Blame**
    
    * Refers to the most recent alteration to every line in the file. Displays Author, Revision, and Time.
        
4. **Commit**
    
    * Record of a moment in Git history containing specifications of a changeset.
        
5. **Checkout**
    
    * Process whereby a particular commit is chosen from the repository, and the condition of the file associated with it and the directory tree are reproduced in the working directory.
        
6. **Diff**
    
    * The difference in changes between saved changes or two Commits.
        
7. **Detached Head**
    
    * State in which a specific commit is checked out rather than a branch.
        
8. **Fetch**
    
    * Retrieves the most recent changes in the branch and the local or remote repositories.
        
9. **Hash**
    
    * Unique SHA1 code for each Commit.
        
10. **Head**
    
    * Name of the Commit at the end of a Branch.
        
11. **Fork**
    
    * When you Fork the repository, you can add Commits and add Pull Requests.
        
12. **Index**
    
    * A group of files that hold state information.
        
13. **Merge**
    
    * Includes changes from named commits (from when their histories split from the current branch) into the current branch.
        
14. **Master**
    
    * Git’s default development Branch.
        
15. **Pull Request**
    
    * Suggests changes to the Master Branch.
        
16. **Repository**
    
    * A group of Commits, Branches, and Tags to identify Commits.
        
17. **Push**
    
    * Pushes new changes once they’ve been committed.
        
18. **Working Tree**
    
    * The directory of files that you are currently working on.
        
19. **Origin**
    
    * Default Upstream Repository.
        

## Git Setup

1. **Initialize an empty Git repository:**
    
    ```bash
    git init
    ```
    
2. **Clone a repository (local or remote via HTTP/SSH):**
    
    ```bash
    git clone [repo / URL]
    ```
    
3. **Clone the repository from GitHub to the project folder:**
    
    ```bash
    git clone [repo / URL] [folder]
    ```
    

## Git Configuration

1. **Configure the username to be used for all actions:**
    
    ```bash
    git config --global user.name "[your_name]"
    ```
    
2. **Configure the email to be used for all actions:**
    
    ```bash
    git config --global user.email "[email_address]"
    ```
    
3. **Create an alias for a Git command:**
    
    ```bash
    git config --global alias.[alias_name] [git_command]
    ```
    
4. **Set a default text editor:**
    
    ```bash
    git config --system core.editor [text_editor]
    ```
    
5. **Open Git’s global configuration file:**
    
    ```bash
    git config --global --edit
    ```
    
6. **Enable the helpful colorization of command line outputs:**
    
    ```bash
    git config --global color.ui auto
    ```
    

## Managing Files

1. **List which files are staged, unstaged, and untracked:**
    
    ```bash
    git status
    ```
    
2. **Show history of changes:**
    
    ```bash
    git log
    ```
    
3. **List all commits from all branches:**
    
    ```bash
    git log --all
    ```
    
4. **Compare two branches by showing which commits from the first branch are missing from the second branch:**
    
    ```bash
    git log [branch1]..[branch2]
    ```
    
5. **To see the difference between the last commit and the working directory:**
    
    ```bash
    git diff HEAD
    ```
    
6. **Display the content and metadata of an object (blob, tree, tag, or commit):**
    
    ```bash
    git show [object]
    ```
    
7. **To see the difference between the working directory and the index:**
    
    ```bash
    git diff
    ```
    
8. **To see the difference between the last commit and the index:**
    
    ```bash
    git diff --cached
    ```
    

## Git Branches

1. **List all branches in the repository:**
    
    ```bash
    git branch
    ```
    
2. **Create a new branch:**
    
    ```bash
    git branch [branch]
    ```
    
3. **List all branches - local and remote:**
    
    ```bash
    git branch -a
    ```
    
4. **List all remote branches:**
    
    ```bash
    git branch -aa
    ```
    
5. **Switch to a branch under a specified name:**
    
    ```bash
    git checkout [branch]
    ```
    
6. **Rename a branch:**
    
    ```bash
    git branch -m [new_branch_name]
    ```
    
7. **Delete a local branch:**
    
    ```bash
    git branch -d [branch]
    ```
    
8. **Merge a branch:**
    
    ```bash
    git merge [branch]
    ```
    

## Making Changes

1. **Add the current changes of a file to staging:**
    
    ```bash
    git add [file/directory]
    ```
    
2. **Add the entire directory changes to staging:**
    
    ```bash
    git add .
    ```
    
3. **Commit the changes with a message:**
    
    ```bash
    git commit -m "[descriptive_message]"
    ```
    

## Rewriting History

1. **Replace the last commit with a combination of the staged changes and the last commit combined:**
    
    ```bash
    git init
    ```
    
2. **Rebase the current branch with the specified base (It can be a branch name, reference to a head, tag, or a commit ID):**
    
    ```bash
    git rebase [base]
    ```
    
3. **Lists changes made to the HEAD of the local repository:**
    
    ```bash
    git reflog
    ```
    

## Undoing Changes

1. **Undo all changes in the specified file/directory by creating a new commit and applying it to the current branch:**
    
    ```bash
    git revert [file/directory]
    ```
    
2. **Unstage the specified file without overwriting changes:**
    
    ```bash
    git reset [file]
    ```
    
3. **Undo all changes that happened after a specified commit:**
    
    ```bash
    git reset [commit]
    ```
    
4. **See which files should be removed from the current directory:**
    
    ```bash
    git clean -n
    ```
    
5. **Remove the unnecessary files in the directory:**
    
    ```bash
    git clean -f
    ```
    

## Remote Repositories

1. **Remove the unnecessary files in the directory:**
    
    ```bash
    git remote add [name] [URL]
    ```
    
2. **Fetch a branch from a remote repository:**
    
    ```bash
    git fetch [remote_repo] [branch]
    ```
    
3. **Fetch the specified repository and merge it with the local copy:**
    
    ```bash
    git pull [remote_repo]
    ```
    
4. **Push a branch to a remote repository with all its commits and objects:**
    
    ```bash
    git push [remote_repo] [branch]
    ```
    

In the fast-paced world of software development, mastering Git is an invaluable skill. With this Git Commands Cheat Sheet, you have a powerful resource at your fingertips to streamline your version control workflow, whether you're a beginner or an experienced developer. Git empowers collaboration, helps you manage your project history, and ensures code integrity.

Remember, Git is not just a tool; it's a journey. As you continue to explore its capabilities and best practices, you'll unlock new ways to work more efficiently and collaboratively with your team. So, keep this cheat sheet handy, and may your coding adventures be filled with success and innovation.

Happy coding! 🚀👨‍💻👩‍💻