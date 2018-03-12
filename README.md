# CMU Science Olympiad Web Platform

## Current Task - Static Website
Our current goal is to build a pretty static website, since we can actually
handle everything else with Google Forms.

## Installation/Development Guide
### Using Git
The master branch is protected, so you cannot push to it directly. Make
a branch off of master by using `git checkout -b <branch_name>`.
Once you are sure your stuff works, merge master into your branch
by typing `git merge master`. Resolve any merge conflicts, then push
and submit a pull request. I will review your changes to make sure everything
looks fine and then merge stuff into master.

### Installation
#### Requirements
- Python 3
- Virtualenv

#### Process
First run `virtualenv venv` to create a virtual environment. Switch to the
virtual environment by typing `source venv/bin/activate`; do this every time
you open a shell to start development. If you see `(venv)` prefixed to your
prompt, you've done everything right so far. Type `pip install -r requirements.txt`
to install all the required packages into your virtual environment. Everything
should be set up now. If you require the use of a new python package, make sure to
run `pip freeze > requirements.txt` in the root directory so the rest of us can
update when we pull as well. When you're done working on this project, type
`deactivate` to get out of the virtual environment.
