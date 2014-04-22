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
