
Create git repo locally

Git is a distributed version control system, so each machine has its own repository. This is different to centralised version control systems like Subversion, which have a single, central, repository.

1. Go to your project

```sh
$ cd my_project
```


2. Initialise the repository

```sh
$ git init
```


3. Add all your files to the repo:

```sh
$ git add *
```


4. Check to see that there are changes to be committed:

```sh
$ git status
```


5. Commit the changes:

```sh
$ git commit -m "First commit"
```


6. Create a public Github project:

```
https://github.com/new
```


7. Add Github as remote origin

```sh
$ git remote add origin https://github.com/yourname/my_project.git
```


8. And finally, push the code to Github:

```sh
$ git push origin master
```