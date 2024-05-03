# General Information

The app-code submodule points to a GitHub with all of the app code. This is the iOS app that sends data to the server which is where the server-code submodule points to.

Go into each submodule for more details about that aspect of the project. 

## Upon cloning
Please recursively clone the contents of the submodules from their remote repository.
```
git submodule update --init --recursive
```
The above command initializes the submodules and then updates them. This is equivalent to the following two commands.
```
git submodule init
```
This command initializes the submodules, preparing them for update. It only needs to be run once, when this repository has just been cloned.

Then,
```
git submodule update --recursive
```
This command performs the actual update for the submodules. Note that this does not mean the submodule is up to date with its respective main branch.

If you only want updates for one submodule, you can use `git submodule update --remote path/to/submodule` instead.

## How to align the submodule branch with its respective main branch.
After updating the submodule, the submodule will point to the branch indicated by the hash you see on GitHub. This might be outdated. If you want the latest changes, simply `cd` into the submodule repository, switch to the main branch, and pull.
```
cd server-code
git checkout main
git pull
git status // should show that it is up to date
```
If you want to update the branch of the submodule being pointed to on GitHub, then you need to push the newly added code after the previous step. In other words, this is to update the hash of the submodule when viewed from the wayfair23-full-project repo.
```
cd wayfair23-full-project // be in the root repo
git add server-code
git commit -m "updated pointer to server-code"
git push
```
Now you will see on GitHub, the submodule is aligned with the main branch of its own repository.
