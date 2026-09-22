---
title: "Getting a Copy of Someone's Project onto Your Own Computer"
author: vinlawz
style: teaching-and-experience
---

# Getting a Copy of Someone's Project onto Your Own Computer

## Introduction

If you find a project on GitHub and want to study it, run it, or build on it, the first step is to get a copy of that project onto your own computer. This article shows you how to do that clearly and confidently, even if you are new to GitHub and the terminal.

## Learning objective

By the end of this tutorial, you will know how to clone a GitHub project to your computer using the recommended GitHub CLI method and an alternative HTTPS method with Git.

## Prerequisites

Before you begin, make sure you have:

- A computer with internet access
- A GitHub project you want to copy
- A **terminal**, which is the application where you type commands. On Windows, you might use Command Prompt, PowerShell, or Windows Terminal. On macOS and Linux, you can use Terminal.
- The **GitHub CLI**, which is GitHub's command-line tool for working with repositories and other GitHub features. You can install it from [https://cli.github.com/](https://cli.github.com/).
- **Git**, if you want to use the HTTPS cloning method instead of GitHub CLI. Git is another tool for working with repositories, and it is required for the `git clone` option shown later in this tutorial.

## What these terms mean

Before we continue, here are a few important words explained in simple language:

- A **repository** is a project folder stored on GitHub. It usually contains the code, files, and history of a project.
- To **clone** a repository means to download a full copy of that project to your own computer.
- A **terminal** is where you type commands to tell your computer what to do.
- **GitHub CLI** is GitHub's command-line tool. It lets you work with GitHub from the terminal.
- A **README** is usually the main introduction file in a repository. It often explains what the project does, how to install it, and how to use it.

## What cloning means

When you clone a repository, you create a copy of the project on your own computer. That makes it easier to read the files, search through the project, run setup commands, and learn how everything fits together.

Cloning does not mean you are taking ownership of the original project. It simply means you now have your own local copy to explore and work with.

## Recommended method: clone with GitHub CLI

The recommended beginner-friendly method in this tutorial is to use GitHub CLI.

### Step 1: Install GitHub CLI

If GitHub CLI is not installed yet, go to the official installation page and follow the instructions for your operating system:

[https://cli.github.com/](https://cli.github.com/)

### Step 2: Find the repository on GitHub

Open the project page on GitHub.

You will see a green **Code** button near the top of the repository page. That button gives you ways to copy the repository address. Depending on the repository and your setup, it can show **HTTPS**, **SSH**, and sometimes **GitHub CLI** clone options.

### Step 3: Run the clone command

Open your terminal and use this pattern:

```bash
gh repo clone owner/repository
```

Replace `owner/repository` with the actual owner name and repository name for the project you want.

For example:

```bash
gh repo clone vinlawz/Maandishi
```

If you want a different project, substitute the owner and repository with the project you actually want to copy.

### Step 4: Wait for the repository to download

After you press **Enter**, GitHub CLI will create a folder on your computer and download the repository into it.

## Alternative method: clone with Git over HTTPS

If you do not want to use GitHub CLI, you can clone the repository with Git over HTTPS instead.

Git is a separate tool from GitHub CLI. Many developers already have Git installed because it is widely used for version control.

From the repository page on GitHub, click the green **Code** button and copy the HTTPS address. Then run:

```bash
git clone https://github.com/owner/repository.git
```

Just like before, replace `owner/repository` with the actual owner and repository for the project you want.

## What to do after cloning

Once the project has been copied to your computer, the next steps are practical and important.

1. Enter the project directory:

   ```bash
   cd Maandishi
   ```

   If you cloned a different project, replace `Maandishi` with the folder name that was created on your computer.

2. Read the `README`.

   The `README` is often the best place to start because it usually explains what the project does, how to install dependencies, and how to run it.

3. Inspect the license.

   Look for a `LICENSE` file or a license section in the `README` so you understand how the project can be used, modified, and shared.

4. Follow the setup instructions.

   Many projects require extra steps after cloning, such as installing dependencies, setting environment variables, or starting a development server.

## Common beginner issues

### GitHub CLI is not installed

If `gh` does not work in your terminal, GitHub CLI may not be installed yet. Install it from:

[https://cli.github.com/](https://cli.github.com/)

Then open a new terminal window and try the command again.

### Permission or private repository problems

If the repository is private, make sure your account has access to it. If you are using GitHub CLI, sign in by running `gh auth login` and follow the prompts before trying to clone again. If you are using Git over HTTPS, use a supported authentication method such as a personal access token or a configured credential manager if Git prompts you for credentials.

### The destination folder already exists

Cloning creates a new folder for the project. If a folder with that name already exists in your current location, the command may fail. You can move to a different directory, rename the existing folder, or choose a clean location before trying again.

## Takeaway

Cloning a repository is one of the most useful beginner skills on GitHub. It gives you a local copy of a project so you can read it carefully, follow the setup instructions, and learn by working directly with real files on your own computer.

Start with the GitHub CLI method if you want the simplest path:

```bash
gh repo clone owner/repository
```

If needed, you can also use Git over HTTPS:

```bash
git clone https://github.com/owner/repository.git
```

Once the project is on your computer, enter the folder, read the `README`, inspect the license, and follow the setup instructions.
