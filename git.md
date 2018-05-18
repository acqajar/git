
# Welcome to Git
#### `**Note: All below assumes Mac users. Sorry :/.`


## What is Git
A version control system that allows you to take "snapshots" of your project. Why is this important? For many reasons, but here are some central ones below:
1. Archive old code
2. If you make a mistake or wrote an enormous amount of unusable code, you can revert back to working code
3. Teams can work collaboratively on some code 

useful links
+ [Git branches](https://gist.github.com/blackfalcon/8428401)
+ [Git workflow](https://guides.github.com/introduction/flow/)




## Table of Contents
  * [Chapter 1 - the Terminal](#chapter-1)
  * [Chapter 2 - Time to Git Installed on Mac OS](#chapter-2)

  * [Chapter 3 - Lets Git started :)](#chapter-3)
  * [Chapter 4 - Sign up on Github ](#chapter-4)
  * [Chapter 5 - Back to the Terminal!](#chapter-5)





## <a id="chapter-1"></a>
### Step 1: The Terminal 
1. To find your terminal, spotlight search for 'terminal' and select it. See below. This is the command line interface tool you will use to control the UNIX-based operating system that the Mac OSX sits on :). If you really want to learn more, [see here](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line).
![Terminal](./png/spotlight.png)

2. Below, is an example of how the terminal will look like. Nice job! You're on your way now to becoming an engineer! :)
![Terminal](./png/terminal.png)
So what are you looking at here? Well, the white space is the `console` - that's where you type commands and see outputs from previously entered commands. The `command line` is where you type your command on the console.

3. Now, for some quick basics regarding the command line that will become important later on (dont worry, we will see them a lot later on as well). Below, are a couple of useful commands:
      + `pwd` = print working directory. In other words, if you want to see where you are, type 'pwd' in the command line and it will give you the directory (or `folder`) you are. See pic below - ![pwd](./png/pwd.png)
      + `ls` will show you the list of files in the directory you are currently in. Again, see image below: ![ls](./png/ls.png)
      + `cd` means "change directory". In other words, if I wanted to change into or go into my "Desktop" directory from the last screenshot, I would type `cd desktop` <a id="touch"></a>`
      + `mkdir` and `touch` are about creating new folders and files respectively.  
      + `echo 'Hello, World.' > first_file.txt` is a command that will "echo" the "Hello, World" string into a new file called "first_file.txt" in your current directory. Now that you've written that string into your newly created text file, you can see it typing `more first_file.txt`.

Awesome! Now we can begin installing Git, our version controll system i.e. VCS. 


## <a id="chapter-2"></a>
### Step 2 - Time to Git Installed on Mac OS

Now in your terminal, at the command line, before you start the process of installing git, check to see if you have Git (in some cases, it might have already come installed given your system configuration). 

To check, on the command line, type `git --version`. 

If not, follow the steps below:

1. [Click here](https://sourceforge.net/projects/git-osx-installer/files/) to start installation. Then follow the prompts to continue installation.
2. Install the `.pkg` file that you downloaded. If you see the following: ![init](./png/init.png) 
Please head to System Preferences —> Security and Privacy —> General tab and click on “Open Anyway” at the bottom. Then continue with your installation. If prompted for your pw, pleasze enter it. Then continue with installation.


3. Check `git --version` once installation is complete. You should see some version installed now. Make sure to set your Git configuration i.e. email and password when prompted.

Keep in mind, some of these instructions might vary for PC. Please click on the [following link](https://www.atlassian.com/git/tutorials/install-git) if you are using a different system.



## <a id="chapter-3"></a>
### Step 3: Lets Git started :)

1. <strong>Git In-it #init</strong><br/>
So you have a  project idea, and you want initialize a `git repository` for your project so you can keep track of the versions. 
So here's a sample of how this might look like below: ![init](./png/init.png)
The commands for what you see in the image above are as follows:<br>
<strong>mkdir [folder_name]</strong><br>
<strong>cd [folder_name]</strong><br>


2. <strong>Create your project </strong> <br/>
Now it's time to add the first file in your folder! To do so, lets start by running the 
[`touch` command](#touch) to create a sample file to upload. In this case, I also wanted to add something to file so I added a sentence by `echo`-ing that sentence into the text file created by the touch command. Last, to make sure the echo worked, I run the following in the command line `more sample.txt`. See image below for more.
![sample](./png/sample.png)
The commands run as follows:
<strong>touch [file_name].txt” e.g. touch file.txt</strong><br>
<strong>echo ‘Hello Everyone :)!’>file.txt</strong>
<br> <br>Also note that the last command will also create the file with the file name and type that come after the arrow. I did it step by step in the above example for clarity :).

3. <strong> Check the Status, Add, and Commit </strong><br/>
To check and see your change, do a git status. You should see the sample.txt file you just created as "untracked", and the file name should appear in red. To begin tracking it, you run the following command:
<br/>`git add -A`<br/>
Then check the status again by running `git status`. At this point, the file should now appear green. See below.
![commit](./png/gitco.png)
Last, run the <strong>git commit -m "[you_custom_message]" </strong>. As seen below:
<br/> `git commit -m "first commit" `
<br/><br/><br/>

#### <strong> Here some of the commands we went over in this chapter for you to review :)</strong>
| Option | Description |
| ------ | -------- |
| git init   | initialize folder as git repository |
| git status | print status of files in repo i.e. shows any changes you've made since your last save/commit  |
| git add  -A| add files to version control|
|git commit -m "[save_message]"| commit i.e. "save" changes|
| git log|  show recent commits|
|git checkout| create or switch branches|
|git merge | merge/combine one branch with another


<br/><br/>
## <a id="chapter-4"></a>
### Step 4: Sign up on Github

1. [Start Here](https://github.com/) and sign up :)
2. Once you're done signing up, start by creating a new repository. There should be a green button the left that says "New Repository" and a plus sign, i.e. +, at the top right near the user icon. Select it and select `new repository`. 
3. On this page, the only item you need to <strong>copy</strong> is the git remote. We will need to modify it slighy for our purposes. <strong> Don’t follow the instructions here. </strong>


<br/><br/>
## <a id="chapter-5"></a>
### Step 5: Back to the Terminal!

Now, back to your terminal. For the git remote, add in the following:

 <strong>`git remote add origin https://[github_usernam]:[github_password]@github.com/[github_username]/[name_of_folder_on_github].git`</strong> <br>
<br>
 if you did add the remote provided by github as is,then you can reset it by using the command below:<br>
 <strong>`git remote set-url origin https://[github_usernam]:[github_password]@github.com/[github_username]/[name_of_folder_on_github].git`</strong>

And finally, you are now ready to execute the last final needed to push to your Github!
<br> <strong>git push -u origin master</strong>
<br/><br/><br/><br/>
![cheetsheet](./png/cheatsheet.png)