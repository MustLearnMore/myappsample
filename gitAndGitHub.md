#Git Basics:

* git init          =   Enter this command whilst in the directory upon which it is 
                        to be applied. This tells the server to initialise Git in 
                        this directory, i.e. have Git *BE PREPARED* to look at all 
                        current and future files/subdirectories in this directory.
                        NB. Git isn't *tracking* any files yet: Git must be explicitly
                        told to track specific files/subdirectories within this 
                        directory.

* git status        =   Asks Git for a status report. E.g. "nothing added to commit
                        but untracked files present". Red text shows files that have
                        been modified but not added/staged for commit. Green text shows
                        files have been modified, added/staged, and are waiting to be
                        committed.
                  
* git add           =   Tells Git to track the file/subdirectory named after the 
                        command (e.g. *git add app.js*), which means it is ready for 
                        a *commit* (see below) in the *staging area*. This must be 
                        done *every time* you want to commit a file/subdirectory. 
                        Multiple files can be added in one go (e.g. git add app.js cats.js),
                        or all files not yet *staged* for commit can be added in one go 
                        by adding a dot to the end of the command, i.e. *git add .*

* git rm -cached index.html     =   Tells Git to remove the specified file (in this                                         case index.html) from the staging area, i.e. the 
                                    opposite of *git add*

* git commit -m "*" =   Tells Git to make a checkpoint in time, recording changes 
                        made up to that point. The *-m* stands for 'message' and
                        allows the user to add a comment (within the quotes) stating 
                        what changes were made in this commit. The convention is 
                        to write these messages in the *present tense*, e.g. "add
                        app file" as opposed to "added app file".

* git log           =   Shows a log of all the changes that have been committed.
                        This will bring up a new command interface with a colon as
                        the prompt, and each of the commits will begin with a long
                        hex identifier. This is important: if you need to go back 
                        to a specific commit, you will need to copy its identifier
                        into the *checkout* command (see below). To come out of the 
                        log, type *q*.
 
* git checkout      =   Tells Git to "check something out." E.g.
                        *git checkout f9656fe992c884ad1bc73f6230874b56848debd0* tells
                        Git to check out the commit with the specified hash.

* *git revert --no-commit 0766c053..HEAD*   =   Not used very often, but noteworthy:
                                                Unlike *checkout*, this actually
                                                reverts back to the commit specified
                                                in the provided hash, and places the
                                                *HEAD* there, much like moving the 
                                                needle on a record. The *--no-commit*
                                                tells Git to commit all commits at
                                                the same time, rather than prompting
                                                the user to confirm at every single
                                                commit.
    
* git push          =   Tells Git to 'push' files to a remote repository, or *repo*.
                        Login credentials will be required, or SSH keys can instead be generated so login isn't required.

* git pull          =   Tells Git to 'pull' latest version of files from a remote 
                        repository.

* git clone         =   Will copy a remote repo into the current folder.

#Adding credentials

* git config --global user.name 'mustLearnMore'
* git config --global user.email 'mustlearnmore@outlook.com'

