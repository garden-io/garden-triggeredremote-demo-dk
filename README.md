# garden-triggeredremote-demo-dk

This is an example of using triggger workflows with remote sources

the main components are:
  - string templating is used in remote source url to allow branch to be set with garden secret
  - custom `garden bump` command used to create empty commit on project repo, that can be used to create a pul request


Typlical work flow
- developer has both project and remote git repos cloned locally
- garden link is used to link remote sources for develeopment
- remote branch (and optionally a pull request) is pushed when wip is ready for review
- garden bump command is used to set secret and push empty commit to proect repo
- pull request created on project repo which trigers workflow
- after review project repo (and optionaly remote repo) pull requests are merged/closed


