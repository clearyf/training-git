README-lab1.txt
===============

NOTE: some mistakes in this document are done on purpose :)

* Clone the repository
  $ git clone https://github.com/clearyf/training-git.git

* Create topic branch
  $ git branch XXX-fix
  $ git checkout XXX-fix

  OR (in one line)

  $ git checkout -b XXX-fix

  OR (newer switch command in one line, fewer footguns)

  $ git switch -c XXX-fix

* Fix a mistake in the provided matterials and commit it
  $ git gui

  OR

  $ git add README-lab1.txt
  $ git commit -m "Insert commit message here"

* If you used the command line experiment with "git checkout", "git
  reset" & "git restore" to move changes in and out of the index.

* If you find change provided on the useful and according to the
  guidelines, please export the patch (format-patch) and send it to
  fionn.cleary@streamunlimited.com

* You should then merge my branch FCL-fix

* Create your own pre merge branch XXX-pre-merge from master
  * Quick
    $ git switch -c XXX-pre-merge master
  * Stupid proof
    $ git switch master
    $ git branch XXX-pre-merge
    $ git switch XXX-pre-merge

* Merge both branches into XXX-pre-merge
  * First merge your own branch from command line
    $ git merge ...
  * Merge the remote branch using the UI and review the incoming patches

* Inspect the results using git blame
  $ git blame README-lab1.txt

* Inspect the history using gitk
  $ gitk --all
