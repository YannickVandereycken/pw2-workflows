# workflows
Workflows for projectweek

## Workflows

### generate-cache.yml

This workflow generates a cache of the projectweek repository. It is triggered when a new ref is pushed to the repository. The workflow will cache maven dependancies when a new branch is pushed to the repository, which will speed up the build process. 

### flow-test.yml

This workflow runs the tests for the projectweek repository. It is triggered when there's a push to master or a pull request is made to master. Builds and unit tests are run and reported on the action.

### async-build.yml

This workflow builds the projectweek repository. It is triggered when there's a push to master. Tests and builds are run async, if both are successful the build is deployed pushed to the registry under `stable:latest`.

