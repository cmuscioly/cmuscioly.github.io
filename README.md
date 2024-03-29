# CMU Science Olympiad Web Platform

## Current Task - Static Website
Our current goal is to build a pretty static website, since we can actually
handle everything else with Google Forms.

## Installation/Development Guide
### Using Git

1. Clone the repository: `git clone <repo-link>`. You can get
the link by clicking the "clone or download" button above
2. Right after you clone, you should be on a branch called `master`. You
can verify this by typing `git branch` and ensuring that the starred branch
is called `master`.
3. Make a new branch for development by typing `git checkout -b <branch-name>`.
This is so that you can develop your features locally at the same time as
other people without producing conflicting stuff. Whenever you make a new
branch to start developing a feature, make sure that `master` is up to date.
Do this by running `git pull origin master` while on the `master` branch.
4. Develop normally using `git`. Specifically, whenever you come to a saving
point that you might want to return to later, use `git add` to choose the files
you want to save, and use `git commit` to save them. This part is pretty
simple; you can look up commands if you need more details. [Here](https://www.git-tower.com/learn/git/ebook/en/command-line/introduction) is
a decent resource.
5. When you are done with you're feature and ready to publish it, you first
have to make sure that you have the updates that other people have made to
`master`. To do this, while you are on the branch you created, type
`git pull origin master`. You may get "merge conflicts" - these happen when
someone else has changed the same file you changed to create your feature.
In this case, type `git status` to see the files marked "both modified" - these
are the ones that have conflicts. If you look inside the files, you should
see what edits you made, what edits other people made, along with some
annotations from git. Edit the file so it contains what you want to keep,
and add it and commit as usual.
6. Once you've merged master successfully, push your changes to the repository
via `git push --set-upstream origin <branch-name>`.
7. Go to GitHub; you should see that you pushed to a branch. Submit a pull
request from your branch to `master`. I will review your changes to make
sure that nothing breaks; then I will merge your changes into `master`. Soon
after, you'll be able to view the website at https://c-er.github.io/cmuscioly-web-platform.

### Installation of Jekyll
Jekyll is a framework that allows us to separate templates (how the website looks)
from the content. This makes it easier to add content, reduces code duplication,
and generally makes everything more elegant.
1. Install [ruby](https://www.ruby-lang.org/en/documentation/installation/)
and the [rubygems package manager](https://rubygems.org/pages/download).
2. Install bundler by running `gem install bundler`.
3. While in the directory where this repository is cloned, run `bundle install`.
4. Whenever you want to view the website, run `bundle exec jekyll serve`. You
will be able to view the website (by default) at `localhost:4000`.