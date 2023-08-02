# How to start use Git and GitHub guide for Mac users
*Hi everyone!*  
This file I'll try to make a mini-guide how to use Git and GitHub (due to this is some like hometask and practice)  
Git - is a tool for control all changes of your project. Instead of having plenty of files like "doc1_v1", "doc2_v2" you allow to have only last version, meanwhile git have info about all of changes which have been made by you and other programmes. So, let's start...  
Best Git tutorial for Russian speakers - [link](https://practicum.yandex.ru/trainer/git-basics/lesson/c6b9607c-e8bc-4446-89f9-c74522c3492f/)  
Markdown tips (md) - [link](https://www.markdownguide.org/cheat-sheet/)

## Begining  
Firstly, you will have to open terminal (*cmd* + *space* and then type "terminal")  
In the programm you can create files, change directory like on the desktop, howevere there is no GUI, instead u can do much more functions, in way you now special commands.  
__*There are fist TERMINAL commands you need at start:*__
* **pwd** (print working directory) demonstrane name of current folder
* **ls** (list) - showing list of files/forlders of current folder
* **cd** (change direction); cd~ - change direction to the home folder of user
* **&&** - do several commands. Example: cd ~ && ls
* **mkdir** - make a new direction (folder)
* **rm** - remove file
* **rm -r** -remove something + *r*ecursive (usually usus for non empty folders)
* **rmdir** - remove direction (folder)
* **clear** - clearing terminal
* **history** - show you history of your commands
* **less** "filename" - demostrate content of  file (only text format)
* **nano** "filename" - we open *filename* file and it's possible to change it inside terminal window (don't forget to save it)
* **cp** "filename" "directory" - copying file in another *directory*
* **mv** "filename" "directory" - moving file in another *directory*
---
***Git commands:***
- **git version** - chking for availability (наличие) of git and version which you have
- **git init** - here u can creaate ypur local repository
- **git status** - cheking for status of files and commit
- **git add** -all, ., filename - preparing and adding your  all changed files, all in folder and certain file for beeing commited
- **git commit** -m "message" - commit ypur pack of files to your repositoty with message wich desribing of commit
- **git commit --amend --no-edit** - edit your last commit without adding new. Be careful - your chash will be changed
- **git commit --amend -m 'new message for the last commit'** - using this function you are able to change message of the last commit without adding new commit
- **git branch** - openning list of all branches
- **git checkout** "branch_name" - move to *bracnh_name* branch
- **git checkout** "branch_name -D - deleting *bracnh_name* 
- **git checkout** "branch_name -b - creating and moving to *bracnh_name*
- **git remote add** origin "repository_link" - The command needs to pass two parameters: the name of the remote repository and its URL. Use the word origin as the name. And you copied the URL from the page of the remote repository.
---
Creating SSH-key:
* **ssh-keygen -t ed25519** "your_mail_in_github@mail.com" - creating public and private key by using programm shh
* **ssh-keygen -t rsa -b 4096** "your_mail_in_github@mail.com" - creating public and private key by using algorithm rsa
---
**GUIDE:**
all points u must to do in terminal
1. Create new folder and create local repository
2. Create new file and change it somehow inside
3. Add and commit it
4. Create new repository in your GitHub profile
5. Now create public and private ssh or rsa keys, they are located in /~/.ssh by default
6. Conncect SSH key to your repository  
    <dr>Copy all you have from public key /~/.ssh/ sshkey.pub  
    <dr>Create SSH key in GitHub settings by pasting info from public key  

6. Connect your local repository with yout GitHub repository
7. Sync local and GitHub repositories by pushing your local commit (git push -u origin master) -  говорим, чтобы терминал запомнил, что надо отправлять на сервер ориджин в ветку master  
8. Check what u have same files in web