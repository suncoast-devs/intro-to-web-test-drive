# Cheat Sheet

## Git

[How to Keep a downstream git repo current with upstream](https://medium.com/sweetmeat/how-to-keep-a-downstream-git-repository-current-with-upstream-repository-changes-10b76fad6d97)

## [Hub](https://hub.github.com/)

### clone your own project

$ hub clone dotfiles
→ git clone git://github.com/YOUR_USER/dotfiles.git

### clone another project

$ hub clone github/hub
→ git clone git://github.com/github/hub.git

### open the current project's issues page

$ hub browse -- issues
→ open [https://github.com/github/hub/issues](https://github.com/github/hub/issues)

### open another project's wiki

$ hub browse mojombo/jekyll wiki
→ open [https://github.com/mojombo/jekyll/wiki](https://github.com/mojombo/jekyll/wiki)

### Example workflow for contributing to a project

$ hub clone github/hub
$ cd hub

#### create a topic branch

$ git checkout -b feature

#### make some changes...

$ git commit -m "done with feature"

#### It's time to fork the repo!

$ hub fork --remote-name=origin
→ (forking repo on GitHub...)
→ git remote add origin git@github.com:YOUR_USER/hub.git

#### push the changes to your new remote

$ git push origin feature

#### open a pull request for the topic branch you've just pushed

$ hub pull-request
→ (opens a text editor for your pull request message)