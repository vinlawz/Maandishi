# The GitHub CLI: gh repo

With this GitHub CLI command, you can create, clone, view and fork a GitHub repository.

```
gh repo create
gh repo view
gh repo fork
gh repo clone
```

## gh repo create

This creates a new repository on your GitHub

>I just realized that I couldn't create a repository using the `gh repo create` without initializing git in the working directory (folder).

First you initialize git in your project folder, simply by:

`git init`

After that, you can now start the process, open the folder on your terminal or cmd and type in the command:

`gh repo create`

First you'll be asked to enter the name of the repo, by default the name of the current folder will be the repo name, then the description of the repo and the visibility of the repository.

Once you are done, tap on <kbd>Enter</kbd> and confirm your details. The repo will be created for you, from the terminal.

[Learn more about `gh repo create`](https://cli.github.com/manual/gh_repo_create)

## gh repo view

`gh repo view`

This command gives you a web view of your repository on the GitHub website.
By default, it will show on the terminal, if your repo has a README.md file, the preview will be displayed on your terminal.

To view directly on the browser, use the command:

`gh repo view --web`

After executing the command, you'll be taken to the web page of the repository

[Learn more about `gh repo view`](https://cli.github.com/manual/gh_repo_view)

## gh repo clone

`gh repo clone`

This is used to clone a repository remotely.

Syntax:

`gh repo clone {GitHub username}/{repository}`

[Learn more about `gh repo clone`](https://cli.github.com/manual/gh_repo_clone)

### Conclusion

GitHub CLI is a very useful tool that saves time and lets you work directly from your terminal.

To learn more on `gh repo clone` command, and all available commands visit the manual page [https://cli.GitHub.com/manual](https://cli.GitHub.com/manual)
