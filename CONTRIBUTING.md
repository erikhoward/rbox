# rBox  Contribution Guide

`rBox` welcomes your contribution. To make the process as smooth as possible, we recommend you read this contribution guide.

## Contribution Workflow
* Have idea for a new feature, bug fix, documentation, etc
* For the `rBox` GitHub repository
* Make your changes in a branch
* Test and or review your changes
* Send a pull request

Here are the steps in detail:

### Setup your rBox Repository

For the [rBox](https://github.com/erikhoward/rbox/fork) source repository. Copy the url of your **rBox** fork. You will need this information later.

```sh
$ cd $HOME
$ git clone <paste saved URL to personal forked rBox repo>
$ cd rbox
```

### Setup git remote as ``upstream``
```sh
$ cd $HOME/rbox
$ git remote add upstream https://github.com/erikhoward/rbox
$ git fetch upstream
$ git merge upstream/master
...
```

### Create your feature branch
Before making code or documentation changes, make sure you create a separate branch for these changes

```
$ git checkout -b my-new-feature
```

### Test **rBox** changes
After your code changes, make sure to:
* Add test cases for the change if applicable
* Review documentation changes for grammar and spelling

### Commit changes
After verification, commit your changes. This is a [great post](https://chris.beams.io/posts/git-commit/) on how to write useful commit messages

```
$ git commit -am 'Add some feature'
```

### Push to the branch
Push your locally committed changes to the remote origin (your fork)
```
$ git push origin my-new-feature
```

### Create a Pull Request
Pull requests can be created via GitHub. Refer to [this document](https://help.github.com/articles/creating-a-pull-request/) for detailed steps on how to create a pull request. After a Pull Request gets peer reviewed and approved, it will be merged.