# Setting up a dev container for Go

* Primary author: [Simon Felt](https://github.com/simofel)
* Reviewer: [Joseph Clampett](https://github.com/josephclampett-education)


## What You Need to start

1. [**Git**](https://code.visualstudio.com/docs/sourcecontrol/intro-to-git) intalled
2. [**Visual Studio Code**](https://code.visualstudio.com/)
3. A **[GitHub](https://github.com/)** account
4. [**Docker**](https://www.docker.com/products/docker-desktop/) installed

## Setting up your repository with your terminal

- Open your terminal
- Navigate to where you want your project stored
- Make your directory and enter it
```bash
mkdir go-project
cd go-project
```
- Initialize your git repository
```bash
git init
```
- Make it into a GitHub repository
```bash
gh repo create go-project --public --source=. --remote=origin 
```

- Create a README.md and push it to your remote repository
```bash
echo "# go-project" >> README.md
git add .
git commmit -m "Initial commit"
git push --set-upstream origin main
```

## Setting up your dev container
