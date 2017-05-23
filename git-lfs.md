# Git Large-File-Storage (LFS)
Working with large files in git is can be problematic.
1. Cloning can get very slow
2. Git / GitHub will slow down trying to manage large diffs for non-binary files.

The [official guide](https://github.com/git-lfs/git-lfs/wiki/Tutorial) can be found here.

_Dig deeper on LFS use of pointers._

## Set-up
* Install `brew install git-lfs`. 
* Set something to track `*.bin`. LFS will make this setting project wide by adding a `.gitattributes` file.
* Commit the file as you would any other
* ??? set up LFS for your repo
* Push

## Pulling
`git lfs ls-files` to see current files in LFS.
`git lfs fetch --all` when on a fast connection and wanting to pull in all files.
`git lfs pull` grab large files for the current branch
