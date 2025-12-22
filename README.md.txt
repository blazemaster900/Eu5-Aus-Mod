How to update the mod git branches:

1) Add the new EU5 version to the git repo

 1.1) Check out a new branch. Branch name would be the EU5 version, eg. 1.0.10
	git switch --orphan <branch name>

 1.2) Copy and commit all EU5 files (except GFX)

2) Check out the current main branch with all mod changes. Check the current TOP commit of the mod
	eg. If the mod was last updated for 1.0.9, <old EU5 version> would be 1.0.9

3) Rebase all mod changes onto the new EU5 version:
git rebase --onto <new EU5 version> <old EU5 version>

	Note: In git terms, this takes commits after the old parent commit and puts them onto the new parent commit
	git rebase --onto <desired new parent commit> <old parent commit>

4) Resolve merge conflicts etc and hopefully there are no issues in-game


BRANCH NAMING
main: Primary mod branch, with all changes

<version names> eg 1.0.9, 1.0.10 etc: EU5 file commits, with no changes