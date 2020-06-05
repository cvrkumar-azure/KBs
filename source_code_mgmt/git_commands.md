# Git



## Installation

### Linux:

#### Ubuntu/Debian : 
```bash
sudo apt update -y
sudo apt install git -y
```

#### Centos/RHEL

```bash
sudo yum update -y 
sudo yum install git -y
```

#### Windows

Go to [Git downloads page](https://git-scm.com/download/win)  and save the file and run it.


## Setup

Once you install git on your computer, configure your name and email

```bash
git config --global user.name <your_name>
git config --global user.email <your_email>
```

## Using Git to track your projects

Create a project folder for your project, or if you have an existing folder `cd` into it.

To start version controlling your folder use the below command:

```bash
git init
```

Create a file and start tracking it.
```bash
git add <filename>  
```

If you have multiple files you can add all of them to git tracking by 
```bash
git add -A 							
```

To save the changes as a commit, run the below command
```bash
git commit -m <commit message>
```
Note: Commit message helps in identifying the changes that you've made, so use meaningful commit messages.

To see the current git tracking status of your folder:

```bash
git status
```

To see all the previous commits 
```bash
git log
```

Revert to a previous commit

```bash
git reset --hard 50ef339dd3d78af6fc11e7ce9b5ea6acc4272e76    
```

## Working with github.

After creating a github account (in your organization, you will be given access to an existing Github account), you need to add SSH Keys to github to authenticate.



### Adding SSH-Keys to Github

1. On your local machine generate ssh-keys.

```bash
ssh-keygen
```

Note: windows users can generate ssh-keys using gitbash.


2. Copy the contents of  ssh public key (In Linux based OS it is generally created at $HOME/.ssh/id_rsa.pub, on Windows c:\users\<username>\.ssh\id_rsa.pub).

3. In Github, click on the user icon at top right corner and click on Settings. In settings click on SSH and GPG Keys.
4. Add the contents of the SSH key under SSH keys.
5. Your computer can authenticate with github wiht ssh keys


### Creating a Repository



### Pushing code from your computer to github repository 

Once a repository is created in github, do the following on your local machine:

1. Go to the project folder, make sure you have a clean working tree and nothing to commit. you check this by using `git status`. If not add everything to tracking and commit it:
```bash
git add -A
git commit -m "<Commit message>"
```

Now add the remote repository with the below command:

```bash
git remote add origin <github_repoURL>

#example
git remote add origin git@github.com:kiranbaddi/gitdemo.git
```




## Branching


List out all current branches

```bash
git branch
```

```bash
git checkout -b feature-212
```




### Delete a branch from local system and remote system

```bash
git push --delete <remote_name> <branch_name>
```

Example

```bash
git push --delete origin feature-xyz
```

