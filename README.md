# The Basics of GitHub

Git is a distributed Version Control System (VCS), which means it is a useful tool for easily tracking changes to your code, collaborating, and sharing. With Git you can track the changes you make to your project so you always have a record of what you’ve worked on and can easily revert back to an older version if need be. It also makes working with others easier—groups of people can work together on the same project and merge their changes into one final source.

These are instructions on how to work with GitHub. Before proceeding, make sure that you have the following setup:

- Your [local development environment](https://docs.google.com/document/d/140jEi-QY2gCjiQ8Qbi7BuEOaEHQ6UFc0riZlkPmict4/edit?usp=sharing) properly set up with Visual Studio Code, Python, and Git installed.
- An account on GitHub set up with your @ycdsbk12.ca account.
- Your GitHub username and email address.

## 1. Fork the repository (optional)
If you're using a repository (or "repo") provided to you from GitHub Classroom, you can skip this step.

If you've been given a repository to copy, you will need to create a fork of it. Your forked repo will be stored in your own personal GitHub account.

![forking](images/01.gif)

## 2. Clone your repository to Visual Studio Code
Cloning your repo to Visual Studio Code creates a local, offline copy on your machine. To do this, follow these steps:

1. From the GitHub page for the repo, copy the URL for your fork to the clipboard:

![cloning](images/02.gif)

2. Next, open Visual Studio Code. Go to **File** > **New Window** in the menu bar.
3. In the new Visual Studio Code window, click on **Clone Git Repository**.
4. Paste the URL from the clipboard into the prompt and press return.
5. You'll be asked where you want to save this cloned folder. (In the example below, I've chosen my *Documents* folder.)
6. Open your cloned repository.

![vs_code_cloning](images/03.gif)

## 3. Edit your code
The Explorer sidebar on the left shows all of the files in the current repo. Begin editing your code by opening the appropriate file in the code editor:

![vs_code_editing](images/04.gif)

## 4. Run your code
Click on the *Run* icon in the top-right corner of the code editor to run your code. A terminal window will appear with your output.

NOTE: Try not to confuse the terminal's command prompt with the actual code output. The command prompt will usually have the hostname of your machine and your username.

![vs_code_editing](images/05A.gif)

## 5. Commit and sync your changes to GitHub
When you are finished editing your code, you will want to Commit and Sync your changes back to the GitHub repo online. 

- **Commit**: This action records a *snapshot* of your changes. When you commit changes, you are creating a *checkpoint* with a *short message* describing the changes you made.
- **Push**: This action uploads the committed changes from your local repository to the remote repository on GitHub.
- **Pull**: This action downloads any new changes from the remote repository since the last sync or clone. New changes are merged with your local repository, warning you of any conflicts.
- **Sync**: This action is combination of all of the above. A *Sync* action will commit and push local changes to the remote repo, as well as pull any new changes from the remote repository.

To Commit and Sync changes, do the following:

1. In the sidebar, click on the **Source Control** view.
2. You should see a list of **Changes** that will be a part of this Commit action. Think of it as a *snapshot of changes*.
3. Type a short message in the **Message** box, describing the changes made. *IMPORTANT: YOU **MUST** TYPE A COMMIT MESSAGE!*
4. Click on **Commit** to record the snapshot.
5. Next, click on **Sync** — a combined **Push** and **Pull** action — to push the changes to the GitHub repo online.

![commit](images/commit.gif)

Note that we have yet to deal with other situations including merging and resolving conflicts. More to come.

### First Commit? How to fix the GitHub configuration error
When you try to do your first GitHub commit in Visual Studio Code, you will get a GitHub configuration error like this:

![error](images/username_error.png)

To fix this, enter the following two commands into the terminal, replacing `your_github_username` and `your_github_account_email` with your own:

```shell
git config --global user.name 'your_github_username'
```
and
```shell
git config --global user.email 'your_github_account_email'
```

For example, my personal setup would look like:

```shell
git config --global user.name 'davecheng-ste'
git config --global user.email 'dave.cheng@ycdsb.ca'
```

And entered into the terminal, it looks like:

![config](images/config.png)

Next, try to run the Commit and Sync actions again. You should then be directed to a web browser to authenticate your GitHub username and password for Visual Studio Code.

This setup should only be necessary on your first Commit action.  

## 6. Verify update on GitHub (optional)
Finally, you can check the repository online (i.e. in the cloud) to verify that your latest Commit changes are reflected:

![commit_changes](images/repo_commit.png)

<br><br>
# Terminology of GitHub 
### Repositories
A repository is where your project work happens--think of it as your project folder. It contains all of your project’s files and revision history. You can work within a repository alone or invite others to collaborate with you on those files.

### Cloning
When a repository is created with GitHub, it’s stored remotely in the cloud. You can clone a repository to create a local copy on your computer and then use Git to sync the two. 

### Committing and pushing
Committing and pushing are how you can add the changes you made on your local machine to the remote repository in GitHub. You can make a commit when you have made changes to your project that you want to “checkpoint.” You can also add a helpful commit message to remind yourself or your teammates what work you did (e.g., “Added a README with information about our project”).

### Branches
You can use branches on GitHub to isolate work that you do not want merged into your final project just yet. Branches allow you to develop features, fix bugs, or safely experiment with new ideas in a contained area of your repository. Typically, you might create a new branch from the default branch of your repository, `main`. This makes a new working copy of your repository for you to experiment with. Once your new changes have been reviewed by a teammate, or you are satisfied with them, you can merge your changes into the default branch of your repository.

### Forks
A fork is another way to copy a repository, but is usually used when you want to contribute to someone else’s project. Forking a repository allows you to freely experiment with changes without affecting the original project.

### Pull requests
When working with branches, you can use a pull request to tell others about the changes you want to make and ask for their feedback. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add more changes if need be. You can add specific people as reviewers of your pull request which shows you want their feedback on your changes! Once a pull request is ready-to-go, it can be merged into your main branch.

### Issues
Issues are a way to track enhancements, tasks, or bugs for your work on GitHub. Issues are a great way to keep track of all the tasks you want to work on for your project and let others know what you plan to work on. 
