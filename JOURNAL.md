February 15

- Setup initial project

- Configure first Action 'Github Tag Bump' 

- Deploy to `master`

Note: Repo doesn't have an initial tag yet.

`Tag v0.1.0 created on master` 

- Commit this JOURNAL with keyword '#patch'

- Push to master

`Tag v0.1.1 created on master` 

Note: keyword '#patch' successfully tested

- Configure default bump: patch

Note: works!

- Create feature branch: TestOtherBranch

- Commit and push new branch

Note: did not trigger workflow

- Create release branch (0.2.0) from master

- Create PR from feature branch to release branch

Note: merging the PR did not trigger the workflow. (Because NOT merged to master)

