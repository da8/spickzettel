# git cycle
* git pull
* git status
* git diff
* git add .
* git commit -m "Comment!"
* git push

# git rename file
* git mv <old_filename> <new_filename>

# show available branches
* git branch

# checkout specific branch    
* git checkout BRANCHNAME

# setup git, config git, create ssh-key and add it to GitLab oder GitHub to work with it
* checking if git exists  
    * git --version
* installing/updating anyhow  
    * sudo apt install git
* Configuring Git  
    * git config --global user.name \"\<USER-NAME\>\"  
    * git config --global user.email "\<USER-EMAIL\>"  
* Adding my SSH key to GitLab  
    * cat /home/<USEER>/.ssh/id_rsa.pub  
    * Copy the entire content of the file. In GitLab, go to your profile settings and add the content of the file as a ssh key.

# Resources
* [\[2021\] How to your SSH key for GitLab on Linux](https://medium.com/devops-with-valentine/2021-how-to-your-ssh-key-for-gitlab-on-linux-1b94e2a3a49a)
