# Git and Jira set up demo
This code repository (or "repo") is used as a practice repo to get comfortable with Git.

## Before you start the  actiity ensure a couple things:
1. **If on Windows**,download Git for windows from here. For the download, let the set up settings as the default. The only setting you may want to change is the default text editor. If you are not comforatle with emacs or vim, you can select notepad. However, learning a text editor like vim or emacs is agreat skill to have. 
  If on **Mac or Linux**, ensure git is present by entering 'git --verison' form your terminal. If this does not work, download git for your OS. 
2. [Create a new SSH key for your system](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent). You only need to follow the "Generating a new SSH key" and "Adding your SSH key to the ssh-agent" sections.
3. [Add the new SSH key to your Github account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).
4. Accept the invite to the JIRA page and send Yuvakshi a message on groupme. A new taks willb added for you on the page which you can use for this demo.
Once you have completed the above steps, you are ready to move onto a short activity.

## Activity steps:
1. **git clone:** The first step is create a local copy our common repository into tyour system. In GitBash/terminal, navigate to the directory where you want to create the the git repository. Now, on the [<>Code tab](https://github.com/SWE-BoeingTech-2023-ECE/demo-repository) in github, click on the green Code button. From here copy the ssh link for the repo. 

Enter the following in your terminal:
`git clone git@github.com:SWE-BoeingTech-2023-ECE/demo-repository.git`

2. **Navigating to your Repository:** Once you have cloned the repository to your system, you wan to navigate into it and make changes here. Run the following in your terminal to go into the repo:

  `ls`: This should show you the name of the repository (in this case demo-repository).

  `cd demo-repository`: This allows you to enter the repository directory.

3. **Check git status:** This command allows you to check the current status of your git branch. Run `git status` If you have not made any changes, you should see something like this: 

4. **List branches:** To allow different users to work on different parts of code concurrently, git offers branches. To list the branches in your local repo, run `git branch`. Your current branch will be highlighted with a * next to it. By default, the branch you are on in the main branch. To view the branches in the remote repo run `git branch --remote`

5. **Create new branch:** Now you will create your own branch to work on. For that, run `git branch your_wiscID`. Replace "your_wiscID" with  your wisd ID to create a new branch.git branch your_wiscid

6. **Switch branch:** You can run `git checkout branchname` to switch to a different local branch. If you run `git branch` after a checkout, you should be on the different branch with the * next to the new branch now. This can help ensure that you correctly switched branches.

7. **Create/Edit file:** Open your preffered text editor byt running one of the following commands:
- `notepad  filename.txt`: use this to open/edit file in notepad. You will need to save your changes and exit notepad to return back to your terminal
- `vim filename.txt`: this will open you fiel in vim text editor, This editor mainly on on keyboard input. If you are not to sure how ot use it, start with notepad. If you do however get into vim, just remember  - to exit vim press 'Esc' key then type ":q" and press enter.
  Once you open and editor add a few lines to the text file, save, and exit the editor.
  
8. **Check your changes:** Run `git status` again to check which files have been updated. You should see your new file listed.

9. **Track changes:** You need to indicate to git which changes you want to keep track of. For that run `git add filename` to track changes in your new file.

10. **Ensure files added:** Run `git status` to ensure required files are added.

11. **Commit changes:** Once you are in a state where you want to save your changes to your branch, run `git commit`. This will open up your default editor. Type your commit message, save and exit. Ensure the commit message follws the format mentioned on the ECE repository's home page. You can find the Jira number by accessing .

12. **Set up identity:** Git needs to know who is pushing to a shared repository. To setup this configuration run git `config user.name username` and `git config user.email email`. Replace  username and email with your details that are linked to your github account.

13. **Share your changes:** When you are ready to share your changes wiht everyone, you will push your changes to the remote branch. For this run `git push`.  This will prompt you to setup an upstrteam branch. Just copy and run the command the prompt gives you. You can go to the repository's code page, click on the branches drop down to ensure your local branch was added to the remote and your changes are in the remote repository.

14. **Create pull request:** Once your changes are pushed, we want ot get them peer reviewed and added to the  main code. This can be done by creating a Pull request. On the repository's hime page you can see a Pull Requests tab. Click on that and then click in the new pull request option. The base branch will be whatever you want to merge to (in this case main) adn the compare branch is your branch with the new changes. For the purposes of this demo add Yuvakshi as the reviewer. In other cases add your team lead (Riya or Megan) and Yuvakshi as reviewers. If you want anyone else to review your code feel free to add them as well. Once your code gets approved, it can be merged to the main. [For this activity, please sned Yuvakshi a groupme DM as soon as you complete the activity so your PR can be approved ASAP]

15. Yay! You made your first changes to a shared repository. Most of what you will be doing to make changes and share your code in git follows these steps.
