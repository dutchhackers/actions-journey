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

- Create PR from release branch (0.2.0) to master branch

Note: merging PR did create a new release. However, it ignored the version from the branch name (0.2.0). Instead it created the next patch version.

- Configure Action GitHub Create Tag Release

- Commit and push to master

Note: various errors: yml syntax, previous step->tag reference

Note: succes! Tagging + releasing works

- Add examples folder

- Next challenge: let's try to add an asset to the release

- Focus on Action: [GitHub Action - Release API](https://github.com/marketplace/actions/upload-a-release-asset)

- Add 'upload assets' step

- Add name to 'checkout' step

Note: Adding custom assets works!

- Add more Actions to TOOLS + add example workflow (Upload Assets)

- Finalize version 0.3.0

- Add actions/upload-artifact Action