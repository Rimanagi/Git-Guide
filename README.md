# How to start use Git and GitHub guide for Mac users  
*Hi everyone!*  
  
This file I'll try to make a mini-guide how to use Git and GitHub (due to this is some like home task and practice)  
Git - is a tool for control all changes of your project. Instead of having plenty of files like "doc1_v1", "doc2_v2" you allow to have only last version, meanwhile git have info about all changes which have been made by you and other programmes. So, let's start...  
Best Git tutorial for Russian speakers - [link](https://practicum.yandex.ru/trainer/git-basics/lesson/c6b9607c-e8bc-4446-89f9-c74522c3492f/)  
Markdown tips (md) - [link](https://www.markdownguide.org/cheat-sheet/)  

## Begining  
Firstly, you will have to open terminal (*cmd* + *space* and then type "terminal")  
In the program you can create files, change directory like on the desktop, however there is no GUI, instead u can do much more functions, in way you now special commands.  

__*There are fist TERMINAL commands you need at start:*__
* **pwd** (print working directory) demonstrate name of current folder
* **ls** (list) - showing list of files/folders of current folder
* **cd** (change direction); cd~ - change direction to the home folder of user
* **&&** - do several commands. Example: cd ~ && ls
* **mkdir** - make a new direction (folder)
* **rm** - remove file  
* **rm -r** -remove something + *recursive (usually uses for non-empty folders)
* **rm -rf .git** - deleting git folder if something went wrong. -r - recursively (for deleting all content in folder); - force(u will spike windows like "are u sure u would like to delete this file")
* **rmdir** - remove direction (folder)
* **clear** - clearing terminal
* **history** - show you history of your commands
* **less** "filename" - demonstrate content of  file (only text format)
* **nano** "filename" - we open *filename* file and it's possible to change it inside terminal window (don't forget to save it)
* **cp** "filename" "directory" - copying file in another *directory*
* **mv** "filename" "directory" - moving file in another *directory*
---
***Git commands:***
- **git version** - checking for availability (наличие) of git and version which you have
- **git init** - here u can create your local repository
- **git status** - checking for status of files and commit
- **git add** -all, ., filename - preparing and adding your  all changed files, all in folder and certain file for being committed
- **git commit -m** "message" - commit your pack of files to your repository with message which describing of commit
eсли ввести git commit без флага -m, откроется редактор Vim. Чтобы выйти из него, нажмите клавишу Esc, наберите последовательность символов :q! и нажмите Enter.
- **git commit --amend --no-edit** - edit your last commit without adding new. Be careful - your chash will be changed
- **git commit --amend -m 'new message for the last commit'** - using this function you are able to change message of the last commit without adding new commit
- **git branch** - opening list of all branches
- **git branch <branch/._-name>** - creating a new branch 
- **git branch -D <название_ветки>** - deleting branch after 
- **git checkout -b <название_ветки>** - creating a new branch and instantly moving in this branch
- **git checkout "branch_name"** - move to *branch_name* branch
- **git checkout "branch_name -D** - deleting *branch_name* 
- **git checkout "branch_name -b** - creating and moving to *branch_name*
_ **git diff** - 
- **git remote add** origin "repository_link" - The command needs to pass two parameters: the name of the remote repository and its URL. Use the word origin as the name. And you copied the URL from the page of the remote repository.  
How to roll back if "everything is broken" | [link](https://practicum.yandex.ru/trainer/git-basics/lesson/78d6157b-a248-4c26-a2f8-5b7bdf270bc4/):
- **git reset --hard <commit hash>** - "откатить" commit
- **git restore --staged <file>** - deleting file from staged status (from being ready to be committed) after this func he will be untracked
- **git restore <file>** - Может быть так, что вы случайно изменили файл, который не планировали. Теперь он отображается в Changes not staged for commit (modified). Чтобы вернуть всё «как было», можно выполнить команду  
  
**Working in team:**  
- **git clone** - clone repository from server to your local repository
- fork -(its a integrated) cloning another repository to your github profile where u can change it and clone on your computer
---
**Creating SSH-key:**
* **ssh-keygen -C ed25519** "your_mail_in_github@mail.com" - creating public and private key by using program shh
* **ssh-keygen -C rsa -b 4096** "your_mail_in_github@mail.com" - creating public and private key by using algorithm rsa
---
**GUIDE:**
all points u must do in terminal
1. Create new folder and create local repository
2. Create new file and change it somehow inside
3. Add and commit it
4. Create new repository in your GitHub profile
5. Now create public and private ssh or rsa keys, they are located in /~/.ssh by default
6. Connect SSH key to your repository (in GitHub settings)
    <dr>Copy all you have from public key /~/.ssh/ sshkey.pub  
    <dr>Create SSH key in GitHub settings by pasting info from public key  

7. Connect your local repository with your GitHub repository
8. Sync local and GitHub repositories by pushing your local commit (git push -u origin master) -  говорим, чтобы терминал запомнил, что надо отправлять на сервер ориджин в ветку master  
9. Check that u have same files in web