# Python library Rug generator and editors

This [rug archive](http://docs.atomist.com/) offers a generator, to create a 
Python package linrary project.

## Generate a Python library project

### From an online button

[<img src="https://images.atomist.com/button/create-project.png" width="267" alt="Get Started with Atomist"/>](https://api.atomist.com/v1/projects/generators/d6812a02-54e5-478c-b75a-214329f00a0e)

This will ask you to authorize the [Atomist](https://www.atomist.com/)
application in your GitHub organisation/account then will ask you to provide
a set of parameters to generate the Python library.

Once the project is generated in your GitHub organisation/account, simply
checkout the newly generated project and follow its README to get started.

### From the Atomist bot

From the [Atomist community slack team](https://join.atomist.com/), or if you 
have brought the Atomist bot to your own slack team, simply type 
```@atomist generators python-lib```. This will bring up the python library 
generator. You can either click on the button or type 
```@atomist create python-lib``` to start the workflow.

Once the project is generated in your GitHub organisation/account, simply
checkout the newly generated project and follow its README to get started.

### From the CLI

To generate a project on your local machine, install the 
[Rug CLI](http://docs.atomist.com/rug/rug-cli/) and run:

```
$ rug generate -X --repo --change-dir /tmp atomist-rugs:python-library:NewPythonLibraryProject myproj
```

This creates a directory `/tmp/myproj` where your Python libfrary can now 
be found. It also initializes that directory as a git repository.

## Edit a Python library project

You can now enhance your new project, or an existing one, by going through
editors.

### From the Atomist bot

From the [Atomist community slack team](https://join.atomist.com/), or if you 
have brought the Atomist bot to your own slack team, simply type 
```@atomist editors python-lib```. This will bring up the Python library 
editors.  You can click on the button for any listed editors.

### From the CLI

Using the Rug CLI, type the following:

```
$ rug describe editor atomist-rugs:python-library
```

This will list all available editors for a Python library project. For instance 
to  apply the `AddPythonGitignore` editor, run the next command:

```
$ rug edit -X --change-dir /tmp/myproj atomist-rugs:python-library:AddPythonGitignore
```

This will add the necessary files. You can now use git to review the changes and
commit them as you see fit. You could also have used the `--repo` flag for an
automatic commit done by the CLI.

## Contribute to this rug

This Rug is an evolving project, embrace it so that it can truly help the 
Python community. It's an open source project that welcome contributors.

To do so, add or amend editors following the 
[Rug documentation](http://docs.atomist.com/). Please, do add a Rug test to the
`.atomist/tests` directory and submit PR to this project.

---
Created by Atomist. Need Help? [Join our Slack team](https://join.atomist.com/)