# Setting up a dev container for Go

* Primary author: [Simon Felt](https://github.com/simofel)
* Reviewer: [Joseph Clampett](https://github.com/josephclampett-education)


## What You Need to start

1. [**Git**](https://code.visualstudio.com/docs/sourcecontrol/intro-to-git) installed
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

- Create a README.md
```bash
echo "# go-project" >> README.md
git add .
git commmit -m "Initial commit"
```

## Setting up your dev container

1. Open up your project in VS Code
2. Install the *Dev Containers* extension
3. Create a `.devcontainer ` directory in the root of your project with the file `devcontainer.json` inside
4. paste the following code into your new file:

``` json
{ 
  "name": "Hello 423--GO",
  "image": "mcr.microsoft.com/devcontainers/go:latest",
  "customizations": {
    "vscode": {
      "settings": {},
      "extensions": ["golang.go"]
    }
  },
  "postCreateCommand": "go version"
}
```

Reopen the project in the container by pressing `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac), typing `"Dev Containers: Reopen in Container"`, and selecting the option. This may take a few minutes while the image is downloaded and the requirements are installed.

Once your dev container setup completes, close the current terminal tab (trash can) and open a new terminal pane within VSCode!

## Hello 423 program

1. Create folder to put your new project, name it `hello423`, and in it a new file called `main.go`.
2. In your `main.go` file, write your Go code.

``` Go
package main

import "fmt"

func main(){
    fmt.Println("Hello 423!")
}
```

To run our program, we will have to turn `main.go` into a package!

In your `hello423` folder run the following command:

```bash
go mod init main.go
```
You can now run your main.go file and see what is outputed in your terminal

```bash
go run main.go
```

Congrats!! You just ran your first Go program. Now lets see how to run it with the build command.

Make sure you are still in the `hello423` folder and run the following commands

```bash
go build main.go

```
In your directory, you should see a `main` file appear. This file contains the binary conversion/equivalent of the code you wrote in your `main.go` file now run this command to the compliled main.go

```bash
./main 
```

This command is similar to the gcc command that we learned in 211 but the difference is that the build command automates the entire build process (compiling, linking, and more), while gcc specifically compiles and links source code into executables or libraries.
