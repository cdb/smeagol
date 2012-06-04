mainstay
========
TODO - This

What it does
============

* Sets you up with [homebrew]
* Installs [git] from homebrew, sets up ~/.gitconfig
* Installs [postgresql], [mysql], [redis], [memcached] and [mongodb].  They're all configured to run when you login.
* Installs [rvm] and sets up 1.8.7 to be the default, self manages on 1.9.2 as well
* Installs common ruby gems: rails 3, sinatra, fog, sqlite3, imagemagick, and all that bullshit
* Installs a pretty sane ~/.irbrc
* Installs a [node.js] development environment with [npm]
* Installs a modern [python] environment with [pip]
* Installs an [erlang] environment
* Installs [MacVim] and sets up [janus]

Running
=======

    % EDITOR="vim" \
      GITHUB_USER="fightclub" \
      GITHUB_TOKEN="..." \
      EMAIL="tyler@paperstreetsoap.com" \
      FULLNAME="Tyler Durden" \
      rake mainstay:install

Disabling Services
==================

Mainstay installs a gem called lunchy which makes it trivial to
enable/disable the services that are installed by default.

    % ps auwwx | grep mongo
    me      202   0.2  0.0  2462220   4120   ??  S    Sat03PM  14:08.53 /Users/me/Developer/Cellar/mongodb/1.8.0-x86_64/bin/mongod run --config /Users/me/Developer/Cellar/mongodb/1.8.0-x86_64/mongod.conf
    % lunchy stop mongo
    % ps auwwx | grep mongo
    % lunchy start mongo
    % ps auwwx | grep mongo
    me    21060   0.2  0.0  2462220   3988   ??  R     1:12PM   0:00.34 /Users/me/Developer/Cellar/mongodb/1.8.0-x86_64/bin/mongod run --config /Users/me/Developer/Cellar/mongodb/1.8.0-x86_64/mongod.conf

[git]: http://git-scm.com/
[rvm]: http://rvm.beginrescueend.com
[npm]: http://npmjs.org/
[pip]: http://pypi.python.org/pypi/pip
[mysql]: http://www.mysql.com/
[redis]: http://code.google.com/p/redis/
[janus]: http://github.com/carlhuda/janus
[MacVim]: http://code.google.com/p/macvim/
[erlang]: http://www.erlang.org/
[python]: http://www.python.org
[mongodb]: http://www.mongodb.org/
[node.js]: http://nodejs.org
[homebrew]: http://github.com/mxcl/homebrew
[memcached]: http://memcached.org/
[postgresql]: http://www.postgresql.org/
