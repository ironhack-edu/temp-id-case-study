![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Contributing (for no coders)

### What is a contribution?

Any change you want to make, whether it’s just **fixing the typo** in the lesson, **updating the code**, or **suggesting a minor or major update to any learning unit** is considered a contribution.

### Before we start - vocabulary

- [Git](https://brennan.io/2015/08/07/github-noncoders/#:~:text=Git%2C%20for%20Non%2DCoders,without%20messing%20up%20their%20progress.)
- [GitHub](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=GitHub%20101,their%20peers%20are%20working%20on.)
- [Repository](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=Sometimes%20shortened%20to%20just%20%E2%80%9Crepo,file%20folders%20on%20a%20computer.)
- [Branch](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=Each%20repository%20can%20contain%20multiple,the%20primary%20branch%20if%20desired.)
- [Clone](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=A%20copy%20of%20a%20repository%20that%20is%20hosted%20locally)
- [Commit](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=A%20record%20of%20a%20change%20made%20to%20a%20file%20or%20files%20in%20the%20repository)
- [Fork](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=is%20when%20you%20copy%20another%20user%E2%80%99s%20repository%20to%20your%20own%20account)
- [Pull/push](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=Merging%20changes%20made%20to%20the%20repository%20files%20into%20the%20local%20copy)
- [Pull Request (PR)](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=When%20you%20want%20to%20make%20changes%20to%20a%20repository%20you%E2%80%99re%20working%20on%20as%20part%20of%20a%20collaborative%20project,%20you%20send%20a%20%E2%80%9Cpull%20request.%E2%80%9D)

### What do I have to know to make a contribution?

You will have to have the **`https://github.com/ironhack-edu/temp-id-case-study`** repository (folder) locally on your computer. How to do this? (for no coders)

### Step 1: Fork the repository

Creating a "fork" is producing a personal copy of someone else’s project.

If you forked someone's project, you will be able to push your code (this is called _making pull request_) so the owner of the original project can check it and if they find it useful, use it.

#### How to fork?

Let's use the [HTML exercise](https://github.com/ironhack-labs/lab-html-exercise) repo for this demo.

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_926952599ca89301b826696c209fd338.png)

<br><br>

After clicking on the fork button, you will be presented with the loading screen that will most likely look like this:

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_10963380e2cfbaab068f92027378ebed.png)

<br><br>

After the forking is done successfully, you will be redirected to the **copied repository on your GitHub account**.

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_ab52ba11af58807f2b0ce6bc33eddcd4.png)

That would summarize the forking process.

### Step 2: Clone the repository

Now, on **your GitHub account**, you have access to the copied repository. This will be a repository you will copy (clone) to your local machine and that will be your working area.

#### How to clone repository?

1. Click on the green <span style="background-color: #32CD32; padding: 5px; border-radius: 4px;">**Code**</span> button and copy the link by selecting and copying or by using the clipboard button.

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_d60e750aafbfe7838bbdbf28619561c4.png)

2. Open your terminal and navigate to the location where you want to store the local version of your repository.
3. When you navigated to the correct folder in your terminal run the following command:

```shell
# you will paste the URL from the clipboard instead of the one we gave in this example
$ git clone https://github.com/ironhack-labs/lab-html-exercise
```

### Step 3: Using cloned repository locally

1. Navigate to the cloned repo locally:

```shell
$ cd <name of the cloned folder >
```

2. Create a branch you will be using to make changes:

```shell
$ git checkout -b "branch-name"
```

Open the project in VS Code:

```shell
$ code .
```

### Step 4: Add, commit and push the changes

After you made changes to your project, you can check which files you changed by running again:

```shell
$ git status
```

**To add the changes**:

```shell
$ git add .
```

<small> :+1: The dot represents all files in the current repository.</small>

**To commit changes**:

```shell
$ git commit -m “<your message>”
```

**To push changes**:

```shell
$ git push origin branch-name
```

### Step 5: Create a pull request

After pushing your changes from your local master to the remote master, your commit should be visible on GitHub (the changes you made locally are now available in the GitHub repository as well).

When your commit is successfully pushed to GitHub, you can create a pull request by clicking on the "New pull request" button.

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_4da38401d30beacf8a0f1564ff0b422c.png)

You should add `sandrabosk` as a Reviewer or in the comment field of the Pull Request (with `@sandrabosk`). This way we will be notified that your work is ready to be reviewed.

<br><br>

**Thank you for your contributions!**
