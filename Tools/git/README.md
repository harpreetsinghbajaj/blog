git diff --stat master..28891-iiw-pai-header

The above command outputs the list of files that have undergone changes in between the two branches starting from the common commit point
from which the branch forked out.

 If changed files have been added but not committed and there is a need to come to the unchanged version use the following:
Git reset HEAD <file name>
Git checkout <file name>

 There is a command to fetch the base commit of a branch. Capture that command here
Capture the command to fetch the list of files that will be merged between two branches.
Command to unstage files ready for commit.

 git log --graph --decorate | grep commit | grep \( | head -n2 | tail -n1 | cut -d'(' -f2 | cut -d')' -f1

This command will show the name of the parent branch of a branch.

 git checkout master -- .gitignore

The above command fetches the .gitignore file from the master branch to current branch

 [hsbajaj1@roanoke-vm1 incorrect-logging test]$ git status
# On branch incorrect-logging
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#       ../src/.nfs0000000001378cf100000190


The above type of output shows that even if commit has been added but there was some file that remained opened during the addition
and commit process. Thus the open file shall be taken care.
To find out the names of files that have changed in current branch when compared with master:à
git diff --name-status master


Current Branch Name

git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'

 Files in a commit

git show --pretty="" --name-only commit id
Rollback Commit

git reset --hard commit id
Head will move to the commit id mentioned above and all changes above this commit id will be lost
Email and Username Configuration

git config --global user.email "email@example.com"
git config --global user.name "John Doe"
git commit --amend --reset-author --no-edit
Append changes to commit

git commit --amend
Head Movement

git reflog show HEAD@{now} -10
This commands displays the way head has changed from commit to commit
Rename Branch

git branch -m new_name To rename the current branch
git branch -m existing_branch_name new_branch_name
Delete Stale Remote References

git branch -rd origin/testBranch git remote -v to list all the remote references
List of paths traversed by head

git rev-list master | while read rev; do git ls-tree -lr $rev | cut -c54- | sed -r 's/^ +//g;'; done | sort -u | perl -e 'while (<>) { chomp; @stuff=split("\t");$sums{$stuff[1]} += $stuff[0];} print "$sums{$} $\n" for (keys %sums);' | sort -rn | head -n 20
Find out commit ids

git filter-branch -f --index-filter 'git rm -r --cached --ignore-unmatch integration/uploads/opt/adtran/libs/diameter/libgxserver.so integration/uploads/opt/adtran/libs/diameter/libtlsutil.so' HEAD
Cloning of vssm session manager was slow due to library files not deleted from git though they are absent from code repo

Enable git colors

git config --global color.ui auto
Current Branch

git symbolic-ref HEAD | sed -e 's,./(.),\1,'
Unpushed Branches

git log --branches --not --remotes --no-walk --decorate --oneline | cut -d '(' -f2 | cut -d ')' -f1
Branches with no upstream

git branch -vv | cut -c 3- | grep -v 'origin' | cut -d ' ' -f1


An example of of using CVS and git hand in hand is at Process

 git diff --name-only SHA1 SHA2
to list the name of files that changed between two commits

git show --name-only
to show list of files in last commit


Git clean-fd to clean all the untracked folders and files


git branch --set-upstream-to=origin/develop eh-3k-FT


If you have reset --hard to a previous commit and u want to come back to the upper commit, U can use git reflog to check how the head moved and then use git reset hard to the relevant commit. If changes are uncommitted then u cannot get them back.


git checkout <COMMIT#> <path/to/the/messed/up/file>

 The above command will checkout the file from the commit id provided

green="%{\033[0;32m%}"
white="%{\033[0;37m%}"

parse_git_branch() {
   git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}

export PS1='\n[\[\033[36m\]\w]\e[0;31m$(parse_git_branch)\e[m\[\033[0m\]\n\[\033[1;35m\]\u@\h\[\033[1;33m\]-> \[\033[0m\]'



