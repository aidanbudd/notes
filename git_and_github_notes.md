#git and github notes

###Create a github repo
This is nicely described [here](https://help.github.com/articles/create-a-repo) on the github pages

###Configuring git locally to work with github

I did the following

`git config --global budd.budd "Aidan Budd"`  
`git config --global budd.email "aidan.budd@gmx.de"`  
`git config --global credential.helper osxkeychain`  


###Commit and push a local git dir to a github repo
This comes from the github [create a repo pages](https://help.github.com/articles/create-a-repo)

`$ git add filename`  
`$ git commit -m 'first commit'`  
`$ git remote add origin https://github.com/username/Hello-World.git`  
`$ git push origin master`


###Clone the repo

`$ git clone https://github.com/aidanbudd/notes`


###Push changes to the repo back to github

`$ git add git_and_github_notes.md`  
`$ git commit -m 'adding info on how to clone from github and how to push changes to github'`  

**not then**
`$ git remote add origin https://github.com/aidanbudd/notes`  
which returns the error
`fatal: remote origin already exists.`  

instead, we just do

`$ git push origin master`  

and the changes are moved over successfully!


###Transferring SSH key from one machine for another to run git from another machine

github has [help pages on this topic](https://help.github.com/articles/generating-ssh-keys)

I know I already have an id_rsa.pub file here

`$ cd ~/.ssh`  
`$ ls -al`  

So I 'just" copy the key with
 
`$ pbcopy < ~/.ssh/id_rsa.pub`  

**oops**! No, I didn't have a key pair on my computer yet... so I do

`$ ssh-keygen -t rsa -C "your_email@example.com"`  
`$ ssh-add ~/.ssh/id_rsa`  

**then** I do the pbcopy and add the ssh key to my github account via the browser




