Welcome to MerkMod Roms
=======================


Getting Started
---------------

To get started with MerkMod, you'll need to get familiar with
[Git and Repo](http://source.android.com/download/using-repo).

Please take note that we have two main line branches depending on
which hardware base your phone is working.

If you have a qcom powered device which needs CodeAuroraForum (CAF)
trees please us the android-4.4-caf branch which pulls for the effected packages
the correct caf version for you.

To initialize your local repository using the MerkMod trees, use this command:


for google, exynos and non qcom devices:

	repo init -u git://github.com/MerkMod/android_manifest.git -b android-4.4


for qcom devices which are using CodeAuroraForum trees:

	repo init -u git://github.com/MerkMod/android_manifest.git -b android-4.4-caf



Then sync up with this command:

	repo sync



Submitting Patches
------------------

We're open source, and patches are always welcome!
You can send patches by using these commands:

    cd <workspace>
    cd <project>
    <"make your changes">
    git add -A
    git commit -a
    cd <workspace>
    git push ssh://<username>@review.merkmod.com:29418/<project> HEAD:refs/for/<branch>

Commit your patches in a single commit.

Squash multiple commit using this command:

	git rebase -i HEAD~<# of commits>

If you are going to make extra additions, just repeat steps (Don't repo start again), but instead of

	git commit -a

use

	git commit --amend

Gerrit will recognize it as a new patchset.

To view the status of your and others patches, visit [MerkMod Code Review](review.merkmod.com)
