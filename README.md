## What is Git?
Git is a *open source* ***Distributed Version Control System ( DVCS )*** designed to handle everything from small to very large projects with speed and efficiency created by **Linus Torvalds ( Linux creator ).** 

In other words, Git enables you to store code, track revision history, merge code changes, and revert to earlier code version when needed, creating a colaborative environment to all his collaborators.

### How does it Work?
Git stores your files and their development history in a local repository. Whenever you save changes you have made, Git creates a commit. A commit is a snapshot of current files. These commits are linked with each other, forming a development history graph. It allows us to revert back to the previous commit, compare changes, and view the progress of the development project. The commits are identified by a unique hash which is used to compare and revert the changes made.

![b](https://user-images.githubusercontent.com/102708433/196016877-52049e28-a788-467a-bbd9-a74d92405482.png)

### What are Branches?
**The branches are copies of the source code that works parallel to the main version.** You can either merge these changes to the original copy or just let the branch remain independent. This feature promotes **conflict-free teamwork**. Each developer has his/her task, and by using branches, they can work on the new feature without the interference of other teammates. **Once the task is finished, you can merge new features with the main version (master branch).**

![gagaga](https://user-images.githubusercontent.com/102708433/196016881-f6b1ebb3-3d65-4bca-a503-4eab53061631.png)

In our **master-branch** was made a new feature of our original file, as it was shown in the previous image. However, was defined to our team to make another modification in the file. To avoid any trouble and possible crash or losing the original file, we can create a new branch - **upstream-branch** - to apply theses modifications.

![2das](https://user-images.githubusercontent.com/102708433/196017028-aa6e57e7-101d-4499-b4cc-53608c198fc9.png)

After the verification of the new features made in the file, was concluded that worked without any mistake. Therefore, we can **merge** the new features to the **master-branch** resulting the final version of the file.

### What are Commits?
There are **three states** of files in Git: *modified, staged, and commit.* When you make changes in a file, the changes are saved in the local directory. They are not part of the Git development history. 

To create a *commit*, you need to first **stage changed files**. You can add or remove changes in the staging area and then package these changes as a *commit* with a message describing the changes.  

# 

#### COMMITTED STATE
A file in ***committed state***, any change made to the file have been saved in the ***local repository***. Therefore, making possible to be *pushed* to the ***remote repository*** - enabling to be uploaded on **GitHub**.

# 

#### MODIFIED STATE
A file in ***modified state*** has new features made to the original content, but it's not yet saved. This means that the state of the file has been altered from its previous state in the ***committed state.***

# 

#### STAGED STATE
A file in the ***staged state*** it is ready to be *committed*. In this state, all necessary changes have been made, resulting to move the file to ***committed state.***

# 

![da](https://user-images.githubusercontent.com/102708433/196017216-bb12b0ce-b2a5-4864-9f5e-050019d272c3.png)


### What are the benefits of Git?

* **Track Changes:** It allows developers to view historical changes, making an easy way to identify and fix bugs.
  
* **Team Collaboration:** As individuos, a collaborator can view and focus on your own task using branches, and merge the changes in the main version without any risk of losing the track of the development. In this way, promote an code review and real-time collaboration, making everyone in the same page.
* **Distributed VSC:** In a distributed system, there is no centralized file storage, allowing multiples backups from the same project.

## Collaboration with GitHub
**GitHub** is a ***cloud software development platform***. It is commonly used for **saving files, tracking changes, and collaborating on development projects**. Individuals can contribute to *open-source* projects and bug reports, discuss new projects and discover new tools.  

### Features
**GitHub** also provides various other features that are as important as showcasing a portfolio.

* **Open-source:** **GitHub** provides a complete ecosystem for open-source projects. You can sponsor maintainers, contribute to a project, use the open-source tool in your existing project, and promote your work.
  
* **Community Collaboration:** **GitHub** has become a community platform where issues, feature requests, code, and documentation contributions can be discussed. 
* **Explore:** **GitHub** Explore tab helps you discover new projects, trending tools, and developer events. 
* **GitHub Gists:** You can share the snippet of your code or embed it in a blog or website. 
* **GitHub CLI:** It allows you to perform merge requests, review code, check issues, and monitor progress from the command line program. 
* **Free Storage:** Unlimited private and public repositories storage.
* **Web hosting:** You can publish your portfolio site or documentation. GitHub pages provide easy to build and deploy website experience. 
* **Codespace**: A cloud development environment integrated with your **GitHub** repository. 
* **Project:** A customizable, flexible tool for planning and tracking the work on GitHub.
* **Automation:** **GitHub** Action automates development workflow such as build, test, publish, release, and deployment.
* **Sponsor:** You can support your favorite open-source project or developers by paying a monthly or one-time fee. It also allows developers to use third-party payment platforms such as ko-fi. 

## Conclusion
**GitHub** plays a larger role in promoting *open-source* projects by providing a ***free software development*** ecosystem for all. 

In this article we have learned about **Git** and **GitHub** and why they are important for any kind of project. 

---

## Additional Reference
For more reference about Git and all his functionalities check [Git Official Documentation](https://git-scm.com/doc)
