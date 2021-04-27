## Steps to Contributing

We use [pre-commit](https://pre-commit.com/) package to run our pre-commit hooks. We use black formatter and flake8 linting on each commit. In order to set up pre-commit on your machine, follow the steps here, please note that you only need to run these steps the first time you use pre-commit for this project.

* Update your python environment, and install pre-commit by using
```
$ pip install pre-commit
```
* Set up pre-commit by running following command, this will put pre-commit under your .git/hooks directory.
```
$ pre-commit install
```
```
$ git commit -m "message"
```
* Each time you commit, git will run the pre-commit hooks (black and flake8 for now) on any python files that are getting committed and are part of the git index.  If black modifies/formats the file, or if flake8 finds any linting errors, the commit will not succeed. You will need to stage the file again if black changed the file, or fix the issues identified by flake8 and and stage it again.

* To run pre-commit on all files just run
```
$ pre-commit run --all-files
```
