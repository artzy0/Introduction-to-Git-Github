## Git Install

Git supports all operating systems. You can install it using command-line tools or directly download and install the setup.

|  System  |  Description |
|  ------------- |  ------------- |
|  `GNU/Linux`  | For `Debian/Ubuntu-based` operating systems use `apt-get install git`, and if you are using another `Linux-based system`, check out the complete list of installing commands [here](https://git-scm.com/download/linux). |
|  `MacOS`  |  If you have [homebrew](https://brew.sh) installed, use this command to download and install **Git**: `brew install git`. If it's not the case, check out the complete list of installing commands for `macOS` system [here](https://git-scm.com/download/mac) |
|  `Windows` | Installing **Git** on `Windows` is hassle-free. Just go to the download [page](https://git-scm.com/download/win), click on the specific `Windows` version, and download and install the setup.  |

<br>

> [!Note]
> For more reference on how to install **Git** in your operating system, check *["Git Install Tutorial"](https://www.datacamp.com/tutorial/git-install-tutorial)*

<br>

## Configurations

In addition to configuring a *remote repository* URL, you may also need to set global **Git** configuration options such as *username*, or *email*. The `git config` command lets you configure your **Git** installation (or an individual repository) from the command line on your terminal. This command can define everything from **user info, to preferences, to the behavior of a repository.** 

### Git Configuration Levels and Files

Git stores configuration options in three separate files, which lets you scope options to individual repositories (local), user (Global), or the entire system (system):

|  **Scope**               |   **Description**   |
|  :---                    |  ----         |       
|  `Local`                 |  By default, `git config` will write to a *local level* if no configuration option is passed. Local level configuration is applied to the context repository `git config` gets invoked in.   |
|  `Global`                |  **Global** level configuration is *user-specific*, meaning it is applied to an operating system user. **Global** configuration values are stored in a file that is located in a user's home directory.    |  
|  `System`                |  **System-level** configuration is applied across an *entire machine*. This covers all users on an operating system and all repos. The system level configuration file lives in a `git config` file off the system root path.   |  

> [!NOTE]
> Thus the order of priority for configuration levels is: **local, global, system**. This means when looking for a configuration value, **Git** will start at the local level and bubble up to the system level.

#

### Defining User Information

As you start your first project and any eventually process that you may apply on future, you first need to define the *author name* ( username ) to be used for all *commits* in the current repository. Tipically, it's used the `--global` flag to set configuration profile for the current user which will be use as a identifier of your operations.

#### Defining username
```julia
git config --global user.name "your-user-name"
```

#

#### Defining e-mail
```julia
git config --global user.email "your@email.com"
```

> [!IMPORTANT]
> The *username* and the *e-mail* defined will be used for all *commits* by the current user.

#

#### Defining shortcuts
This is a powerful utility to create custom shortcuts for commonly used *git commands*. Take an example:

```julia
git config --global alis.ci commit
```

This creates a `ci command` that you can execute as a shortcut to `git commit`.

<br>

> For more reference about git shortcuts, check: *["Git Basics - Git Aliases"](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases)*

## Example 
After installing **Git**, the first thing to do it is to define your identification settings, as discussed before. A typical initial configuration might look something like the following:

```julia
git config --global user.name "Nicholas Chiuz"
git config --global user.email "nicholas@example.com"

git config --global alias.co checkout
git config --global alias.st status
```

## Creating a Project

When it comes about creating a new *repository*, you can choose between start a new project through the command inline `git init`, or manually creating a new repository on **GitHub**. For didactic and visual purposes, let's take the second option.

### Creating a new Repository on GitHub

Go to `Your Repositories` page and select the `new` icon to create a *remote repository*.
![261873874-eb00ca2c-743b-4287-8622-a5f9caaffe6d](https://github.com/artghieri/Git-and-GitHub-Introduction/assets/102708433/6c65aaf1-d4b7-4bb1-8e5d-2d3178c9f242)

In this new section, selec the **repository name field** and type ***Git Project***. We'll be using this name to refer to our new project. 
![261873876-0d2df648-0192-44b9-9897-01dcabb465a5](https://github.com/artghieri/Git-and-GitHub-Introduction/assets/102708433/bf5deca8-99ff-4fb3-9f48-62356e3881db)

> [!IMPORTANT]
> **Don't forget to check `"Add a README file"`.**

<br>

Your *public remote repository* might look like the following:

![261871782-0dd6ae39-eb76-4e32-aa7a-75ae7853d068](https://github.com/artghieri/Git-and-GitHub-Introduction/assets/102708433/913be38e-32a9-496d-b20b-0cd64c480543)

## Clonning 

If a project has already been set up in a central repository, the clone command is the most common way for users to obtain a local development clone. `git clone` is primarily used to point to an existing repo and make a clone or copy of that repo at in a new directory, at another location.

The `git clone` command copies an existing **Git** repository making a completely isolated environment from the original repository. As a convenience, cloning automatically creates a remote connection called "origin" pointing back to the original repository. This makes it very easy to interact with a central repository.

```julia
git clone your_repository_url 
```

### Git URLs

**Git** has its own URL syntax which is used to pass remote repository locations to **Git** commands. `git clone` is most commonly used on *remote repositories* and supports a few different network protocols and corresponding URL formats. 

| **Protocol**          |     **Description**        |
| :----------:            | -------                    |
| `SSH`     | **Secure Shell (SSH)** is a authenticated network protocol that is commonly configured by default on most servers. Because SSH is an authenticated protocol, you'll need to establish credentials with the hosting server before connecting. |
| `GIT`     | A protocol unique to git. **Git** comes with a daemon that runs on port (9418). The protocol is similar to SSH however it has no authentification. |
| `HTTPS`   | **Hyper Text Transfer Protocol**. The protocol of the web, most commonly used for transferring web page HTML data over the Internet. | 

<br>

> For more reference, check the documentation *[git-clone](https://git-scm.com/docs/git-clone)*

# 

### Clonning a Remote Repository

To initialize our project, first we need to pull all files from the *remote repository* located on **GitHub**. In this case, we're clonning the *remote repository* by providing an **HTTPs** link.

```julia
git clone https://github.com/username/Git-Project
```

Succeed the cloning of the *remote directory* appointed before, it will be created in your machine a *local repository* of `Git Project`.

![image](https://github.com/artghieri/Student-Guide---The-C-Language/assets/102708433/6559093f-a95a-416d-a728-8581f212ea37)

# 

<br>

## Repository and File Modifications

When working in **Git**, the concept of "saving" is a more nuanced process than saving in a traditional file editing applications. A *commit* is the **Git** equivalent of a "save". Traditional saving should be thought of as a file system operation that is used to overwrite an existing file or write a new file. Alternatively, **Git** *committing* is an operation that acts upon a collection of files and directories.

**Git** *commits* can be captured and built up ***locally***, then pushed to a ***remote server*** as needed using the `git push -u origin main` command. 

A **Git** repository can be configured to ignore specific files or directories. This will prevent **Git** from saving changes to any ignored content. **Git** has multiple methods of configuration that manage the ignore list.

#

### Git Add

The `git add` command adds a change in the **working directory** to the **staging area**. It tells **Git** that you want to include updates to a particular file in the next *commit*. However, `git add` doesn't really affect the repository in any significant way-changes are not actually recorded until you run `git commit`.

In conjunction with these commands, you'll also need `git status` to view the state of the working directory and the staging area.

<br>

> For more reference, check the documentation : *[git-add](https://git-scm.com/docs/git-add)*

#

### Workflow

The `git add` and `git commit` commands compose the fundamental **Git** workflow. They are the means to record versions of a project into the repository’s history.

Developing a project revolves around the basic edit/stage/commit pattern. First, you edit your files in the working directory. When you’re ready to save a copy of the current state of the project, you stage changes with `git add`. After you’re happy with the staged snapshot, you *commit* it to the project history with `git commit`.

In addition to `git add` and `git commit`, a third command `git push` is essential for a complete collaborative **Git** workflow. `git push` is utilized to send the *committed* changes to *remote repositories* for collaboration. 

<br>

> For more reference, check the documentation *[git-commit](https://git-scm.com/docs/git-commit)*

<br>

## Project Modifications

Proceeding the with the work done in the previously topics, after creating a *local repository* and pull all the original files from **Git-Project** that was created in the begining, we'll add a new archive to the project.

Inside the *"Git-Project"* folder, create a `document.txt` with the following text: *My first document*. Might look like the following image:

![image](https://github.com/artghieri/Student-Guide---The-C-Language/assets/102708433/29173016-8e08-4907-bbb0-4a97f21082f2)

Open the `README.md` file and change the text for the following:

```
## Hello World

This is my *first project* using **Git** and **GitHub**.
```

# 

### Adding, Commiting and Pushing Files

After all files modifications has been made, we can *stage* all changes with the command inline `git add .`.

```julia
git add .
```

> [!NOTE]
> You can always check any changes made with `git status` command.

<br>

With `git status` command it's possible to visualize any change that has been made in the files in your *local repository*. As you can see in the expected following message:

```julia
git status
```

```julia
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
        new file:   document.txt
```

Finishing the modifications, we are gonna use the command `git commit` and the command `git push` to update all the modified files in the *local repository* to our *remote repository*.

#

```julia
git commit -m "my first commit"
```

By default, `git commit` will open up the locally configured text editor, and prompt for a *commit* message to be entered. Passing the -m option will forgot the text editor prompt in-favor of an inline message.

#

```julia
git push
```

The `git push` command is used to upload *local repository* content to a *remote repository*. Pushing is how you transfer *commits* from your *local repository* to a *remote repository*. 

`git push` is most commonly used to publish an upload local changes to a central repository. After a local repository has been modified a push is executed to share the modifications with remote team members.

<br>

> For more reference, check the documentation: *[git-push](https://git-scm.com/docs/git-push/en)*

#

#### And our Git-Project might look like this:

![261872174-09295943-95c6-42ae-946a-2bde566fe643](https://github.com/artghieri/Git-and-GitHub-Introduction/assets/102708433/efdcc608-1e07-4050-b515-645edd26c9cd)

## Branches

A branch represents an independent line of development. Branches serve as an abstraction for the edit/stage/commit process. You can think of them as a way to request a brand new working directory, staging area, and project history. New commits are recorded in the history for the current branch, which results in a fork in the history of the project.

The `git branch` command lets you create, list, rename, and delete branches. It doesn’t let you switch between branches or put a forked history back together again. For this reason, `git branch` is tightly integrated with the `git checkout` and `git merge` commands.

<br>

> For more reference, check the documentation: *[git-branch](https://git-scm.com/docs/git-branch)* and *[git-checkout](https://git-scm.com/docs/git-checkout)*

# 

Therefore, we are gonna crete a new branch using `git-checkout` command.

```julia
git checkout -b "new-branch"
```

It's important to understand that branches are just pointers to commits. When you create a branch, all Git needs to do is create a new pointer, it doesn’t change the repository in any other way.

#

Open the `README.md` file in your *local repository* and change the text for the following:

```julia
## World, Hello

This is my *first project* using **Git** and **GitHub**.
```

Now we are gonna *stage* our modification using `git commit` command and update the *remote repository* with `git push`.

```julia
git commit -m "my second commit"
```

```julia
git push origin "new-branch"
```
#

#### And our Git-Project might look like this:

![261872457-155b0c56-163d-40b3-91fe-85002c836ee6](https://github.com/artghieri/Git-and-GitHub-Introduction/assets/102708433/965e7ccb-9164-41e2-a054-5de729e1c06d)

![261872544-934c603e-1137-4c31-924d-1ac47be3d1c6](https://github.com/artghieri/Git-and-GitHub-Introduction/assets/102708433/6aa4ddab-cadc-49fd-9a8d-cb309d40c15b)


## Merging and Pull Request

Merging is Git's way of putting a forked history back together again. The `git merge` command lets you take the independent lines of development created by `git branch` and integrate them into a single branch.

Git merge will combine multiple sequences of commits into one unified history. In the most frequent use cases, `git merge` is used to combine two branches. 

```julia
git merge branch-to-merge
```
> For more reference, check *[git-merge](https://www.w3schools.com/git/git_branch_merge.asp?remote=github)*

<br>

Meanwhile, the `git pull` command is used to fetch and download content from a *remote repository* and immediately update the local repository to match that content. Merging remote upstream changes into your *local repository* is a common task in Git-based collaboration work flows. 

```julia
git pull
```

> For more reference, check *[git-pull](https://www.w3schools.com/git/git_pull.asp?remote=github)*

#

#### In this case the merge and pull request we're made by simply following the steps on **Git Project** *remote repository* as is shown in the following steps after select the `Compare & Pull request` button.

![image](https://github.com/artghieri/Student-Guide---The-C-Language/assets/102708433/45446205-c097-4e34-843f-336c42e5cf28)

![image](https://github.com/artghieri/Student-Guide---The-C-Language/assets/102708433/8d4f0e2b-f342-499e-8ada-332a0788c8f3)

![image](https://github.com/artghieri/Student-Guide---The-C-Language/assets/102708433/7146b9ae-ae09-48dc-976f-adbb3bf727b3)

The `main branch` was merged with the `new-branch`, changing the `main branch` `README.md` file content.

![261872660-70ca5152-3154-41f1-9af1-e006f5b2f3d6](https://github.com/artghieri/Git-and-GitHub-Introduction/assets/102708433/fe2c0f87-dc4b-4e94-847e-02b77abe8fc6)


---
