# Basic Git tutorial

This document explains the basic of Git and GitHub and explains how you can upload your code to GitHub.
If you have any questions, feel free to send me an email at dvspoel@widener.edu

## What’s git?
Git is a type of software that is called a version control system. It’s used by computer science people to keep track of changes made to their code over time.

Imagine you're working on a big project, like a term paper or a group presentation. You and your classmates are all making changes to the same document, but you don't want to accidentally overwrite each other's work or lose any changes that you make. One solution would be to save multiple copies of the document, like "term_paper_v1.docx", "term_paper_v2.docx", and so on. But this can quickly become confusing and disorganized, especially as more people start working on the project.

Git does things differently. Instead of saving multiple copies, Git uses a “repository” that keeps track of all changes made to the code. This is basically a timeline of changes you made to your code. When you make a change to your code, you “commit” it to the repository with a short message describing what you changed. This creates a new point in the timeline of changes. 

Git also allows you to create “branches” This means that you can create a separate version of the code without affecting the main version. This is especially handy if you work with multiple people. Everyone can have their own branch. And when they are finished they can “merge” (combine) their work into the main branch.

## Git vs GitHub
GitHub is one of the more popular places to host git repositories. You can basically see it as the online version of Microsoft word. You also have other platforms, for example, GitLab and BitBucket that do the same but with a different UI and feature set.

I’m explaining GitHub because it’s the most popular one. And in my opinion, it’s the easiest to work with. The benefit of pushing your code to GitHub is that you always have a backup. You even have the ability to publish your work and give access to other people to work together. What important is is that everything you add to git, even after you remove it. Will still be visible! So make sure you don’t accidentally put any passwords or other secrets in a (public) repository. There have been many (big) security incidents because of this.

## actually doing something!
So now that we got the boring theory out of the way. let’s start with the fun part! (Actually doing something)

### 1) Creating a GitHub account
If you already have a GitHub account you can skip this step and just login to your existing account instead

If you go to https://github.com/signup you can create a new account, you will need to provide GitHub with a few details, solve a small puzzle and enter a verification code you got by email from them.

After that, when it’s asking you for more details, you can just scroll down and click “Skip personalization
Then the dashboard will open with a fancy animation and you are set! You can either minimalize or close the browser window.

#### 2) Creating a local repository
Because some of you will be using Linux, and some of you will be using windows. These steps will be a bit different. So if you have any questions please let me, matt, or Evie know!

First, we need to create something to upload to GitHub. Create an empty directory on your desktop, then, in that directory, create an empty file called `README.md`. In this file, you can add a short text, for example, “Welcome to my first git repository” Then you can save and close this file.

After that, you will need to open the directory.
In windows, open the directory and right-click and click on open in terminal
In Linux, open the directory and click on open terminal here

##### Then we are running a few commands, these commands are case-sensitive so please make sure you type everything correctly

First, we are going to create a local repository using `git init`
After that, we are adding the readme file we just created to the git repository. This will make sure any changes we make are tracked. We do this using `git add .` The . stands for everything, You can also only add specific files using `git add youramazingfilename`

After making sure GIT is tracking our changes, we are going to make a commit. We do this using `git commit -m “Your amazing message”` You can replace Your amazing message with whatever you want.

When you make any changes in the future, You will need to run the git add and git commit commands again.

![carbon (3)](https://user-images.githubusercontent.com/28593493/225716371-3112b768-5e22-4652-90de-8f7f57545919.png)

#### 3) Create personal access token
To be able to push things to github, you need to create an access token. To do this follow the following steps:
- CLick on top right profile picture
- click on settings in dropdown
- Click on developer settings (bottom left)
- CLick on Personal access token
- CLick on Token (classic)
- Click on generate token -> generate classic token
- Give the token a name and check "repo"
- CLick on generate token
Copy the token and save it somewhere save. 

#### 4) Creating a remote repository
Log into your GitHub account.
Click on the green “Create repository button”, or if you already have a repository, click on the “New” button in the top left

You need to give your repository a name, and you can leave the rest of the settings on default. If you want you can change the public to private, public means everyone can see the repository and the code, and private only means you can access it.

When you're done you can click on create a repository

A new window will open with a bunch of commands, the only important one is the `git remote add` command. This command tells git to add a new remote to push code to. You can copy this command and execute it in your open terminal

After that, the only thing left is to actually push the code to github, you can do this using the `git push origin master` command.
This command will ask you for a username and password. You can use your github username but you must use the token you created earlier as the password

Refresh your github window. If this now contains your file. Congratulations! You just created your first github repository!

![carbon (4)](https://user-images.githubusercontent.com/28593493/225718475-6aaaaed3-0a14-4b07-9398-8a3af16f8fda.png)
