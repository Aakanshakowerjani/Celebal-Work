# Development

### Configuring Github
 - Create an account on Github.
 - Create a new Repository and copy its url.
 - Install git locally using Command Prompt.
 - Move to directory where your project files are.
 - Clone local repository using following command where link is copied link of your repository:
```sh 
     git clone link
```
 - Change directory to that folder.

### Adding File to Github
 -   Add the project file github .
 -   Commiting the file following with message.
 -   Finally pushing the file to github repo.
 ```sh
     git add filename.ext
     git commit -m "message"
     git push
 ```
 - Go to github repository page and refresh it following changes will reflect.

### Updating the existing file 

  - Pull the project file from github to your local repository :
 ```sh
     git pull
 ```
  - Update the file and push it back to the github by the above adding commands.

### Merge Conflict 
Whenever any two person try to change the file at the same time then there is chances of Merge Conflict.

### Resolving Merge Conflict
 - This is resolve manually.
 - Remove all head and tail and make project as per your requirements.
 - Remove all <<<<<, ====== and >>>>>> and write desirable code.
 - Then push that file again to github.
 
### Git log
 - You can view all the changes you made to your repo by following commands:
```sh
     git log
```
### Git Reset
 - Consider a situation where you made the change to the code and you no longer feel like keeping the change you can always go back to the previous version of the code by the following command:
```sh
     git reset --hard<commit hash value>
```
