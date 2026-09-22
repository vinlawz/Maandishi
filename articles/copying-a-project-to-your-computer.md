---
title: "Getting a Copy of Someone's Project onto Your Own Computer"
author: vinlawz
style: teaching-and-experience
---

# Getting a Copy of Someone's Project onto Your Own Computer

Imagine your friend hands you a recipe book. You do not want to read it once and hand it back. You want your own copy so you can underline things, try recipes at your own pace, and make a few notes in the margins.

That is more or less what it feels like to **clone a repository**.

You are making a copy of someone else's project on your own computer so you can explore it, learn from it, and possibly contribute to it later.

I remember the first time someone told me to "clone a repo." I froze. It sounded like something from a science-fiction film. Was I duplicating a robot? Thankfully, no. In software, **cloning a repository simply means downloading a copy of a project from GitHub to your computer**.

## Why would you want to do this?

There are several very normal reasons:

- You found a project online and want to explore how it works.
- You want to read someone else's code at your own pace.
- You want to experiment without touching the original project on GitHub.
- You want to contribute an improvement, fix, or idea.
- You are learning, and real projects teach a lot.

Reading code on your own computer is often much easier than reading it through a browser tab. You can open files properly, search through folders, and take your time.

## The tool that makes this simple

GitHub has a companion tool called **GitHub CLI**. "CLI" means **Command-Line Interface**, which is just a formal way of saying you type commands into your terminal instead of clicking through menus.

If you do not have it yet, install it from the official GitHub CLI website:

[https://cli.github.com/](https://cli.github.com/)

It is available for Windows, macOS, and Linux.

I know typing commands can feel intimidating at first. I felt that too. But once you do it a few times, it starts to feel less mysterious and more practical.

## Getting started

### 1. Install GitHub CLI

Visit the official installation page and follow the steps for your operating system:

[https://cli.github.com/](https://cli.github.com/)

You only need to do this once.

### 2. Find the repository you want

Go to GitHub and open the project you want to copy to your computer.

On the repository page, look for the green **Code** button. That button can show you different cloning options, such as HTTPS, SSH, and GitHub CLI. It is a useful place to start if you want to see the repository address and the available ways to copy it.

### 3. Clone the repository

If you are using GitHub CLI, the command looks like this:

```bash
gh repo clone owner/repository
```

Replace `owner/repository` with the actual repository you want.

For example, if you wanted to clone this project, you would run:

```bash
gh repo clone vinlawz/Maandishi
```

That example is only for this repository. For any other project, substitute the owner name and repository name with the one you actually want.

### 4. Wait for the download to finish

After you press **Enter**, GitHub CLI will download the project to your computer and create a folder for it.

When it finishes, you now have a local copy of the repository. You can open that folder in your code editor, explore the files, and start learning from what is there.

## What should you do after cloning?

Keep it simple:

- Open the project folder.
- Read the `README` first.
- Look for setup or installation instructions.
- Check the license so you understand how the project can be used and shared.
- Take your time exploring the folders and files.

The `README` is often the friendliest doorway into a project. It usually explains what the software does, how to run it, and any rules or expectations for contributors.

Respecting the license matters too. A public repository is not the same thing as permission to do absolutely anything. Most good projects tell you clearly what is allowed.

## A small personal note

The first time cloning a project worked for me, I remember feeling almost silly afterward. I had built it up in my mind as something only "real developers" knew how to do.

But cloning a project is genuinely one of the friendliest first steps into software. You do not need to understand every file before you begin. You just need enough curiosity to say, "Let me bring this onto my own computer and see what is inside."

## The takeaway

You do not need a technical background to start exploring how software is built.

All you really need is:

- A little courage to type a command,
- A project that interests you,
- And the willingness to learn by doing.

Everything else — understanding the code, making changes, and contributing back — can come after this first small step:

**getting your own copy of something you are curious about.**
