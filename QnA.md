## 01: Question 1:
A Data Engineer discovers a critical bug in the production data transformation pipeline managed in a Git repository on the `master` branch.
To comply with the company's policy of using feature branches for bug fixes and enhancements, 
which sequence of Git commands should the engineer use to set up their development environment to address this issue?
      ## ANS: git clone followed by  git checkout -b 
         The `git clone` command is used to make a local copy of the specified repository. Following this, the `git checkout -b` 
         command creates a new branch and switches to it immediately.
         This sequence is appropriate for starting work on a new branch, such as a hotfix branch, directly after cloning a repository.
            
