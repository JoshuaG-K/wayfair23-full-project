# General Information

The app-code submodule points to a GitHub with all of the app code. This is the iOS app that sends data to the server which is where the server-code submodule points to.

Go into each submodule for more details about that aspect of the project. 

## How to use Github submodules
Don't let the idea of GitHub submodules intimidate you! The submodule is just a pointer to a certain commit in another remote repository. You can change this commit that the submodule points to with the command `git submodule update --remote path/to/submodule` where path/to/submodule is the path to the submodule folder on your local machine.  However, note that this method implies that the remote repository that we are pointing to has been updated. Thus you need to update the repository being pointed to before you update the submodule. Let's give an example. We will call the remote repository with our submodules repoA and the repository that is one of the submodules repoB. We made changes to repoB and pushed them to repoB's remote. We want these changes to show up in the submodule in repoA. Because the changes are pushed to repoB's remote, we can do the command `git submodule update --remote path/to/submodule` to update repoA to point to the latest commit on the remote repository for repoB.
