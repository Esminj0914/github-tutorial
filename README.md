# GitHub Tutorial

_by Esmin Jusic_  

---
## Git vs. GitHub
**Github:** Github is the website in which someone can put their work on so that anyone can see it.

**Git:** Git is the code and it can be used to put work that people have done onto github.

**Relationship:** Git does not need github in order to work but github needs git in order to work.  


---
## Initial Setup
1 Make an account on github.com   
2 Setup your IDE. [Just click here and follow the instructions.](https://github.com/hstatsep/ide50/blob/master/README.md)  
3 If you ever want to clone a project from github make sure that you use the SSH key link. This is important because if you use HTTPS you have to log back in everytime. 

---
## Repository Setup
A repository is a folder that is connected to github. In order to make a file into a repository you want to make sure that you are in the file and then do `git init` to turn it into a repository. You will know that you did it correctly if you see `(master)` after the folder name. 

**Example :** `~/fruits/apples/ (master) $`

When you initalize a folder into a repository you also want to create a repository with the same name on github. When you log in on github.com you should see repositories on the left side and you can press the green button to create a new repository. Make sure to have your repo named exactly as it is named in your ide. 

When you work on your ide you might want to upload the work you have done to github.com. In order to do this you have to put in a command that allows you to push all your work to github. To do this do `git remote add origin (take the link of your repo on github).git ` then `git push -u orgin master`. You are now set up to push from your ide. 

When you are done editing a file you can use `git add (file name)`, then you can do `git commit -m"you can put a message here but make it past tense"`. If you are ready to put that work into github then you can do `git push` 

---
## Workflow & Commands
Now that you finished your inital setup and your repository setup you are now ready to learn some basic commands you will need when using your ide. 

`git add(file name)`-When you do git add you are preparing files to be commited.   
`git commit -m`-When you are ready to save all the files that you have added then you do git commit.  
`git status`-Shows the changes that have been made since the last commit.   
`git push`-Takes your last commit and pushes it to github so that people can see your work.  


---
## Rolling Back Changes
While you work in your ide you can make some mistakes that you might want to undo. Here are ways to undo some errors

`git reset HEAD (file)`- When you accidently use `git add` to a file that you dont want to commit. 

`git checkout (file)`- When you want to undo changes to a file. 

`git rest HEAD~`-When you want to undo a commit.

In order to undo a push you have to choose one of your previous commits that you will like to go back to. First do `git log`, find which commit you want to go back to and copy the sha key. then do `git revert (sha key)` and it will take you back to that commit and undo the push.



---
## Error Handling 
If you accidently do git init in the wrong repository you can do `rm -rf .git`. 

If you want to remove a repository you can do it two ways. 
1) On github.com you can go to the repository settings and delete the repo.  
2) In your ide you can uninitialize the repo and delete the folder by using rm -rf. 



