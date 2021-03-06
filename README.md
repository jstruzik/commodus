# Robinpowered Commodus
A sinatra powered, heroku ready application that will track open pull requests, and search comments for the :+1:

![](http://3.bp.blogspot.com/-CmAKAZkYCtQ/UFHmbs36DXI/AAAAAAAAC4M/QCtrQRcmoBk/s1600/thumbs-up-gladiator.gif)

## Usage

Simply run `bundler install` and `ruby app.rb` to startup the sinatra app locally.

Use `git push heroku master` after cloning to deploy to a heroku server.

Setup a personal access token with `repo` scope with `export ACCESS_TOKEN=token` or `heroku config:set ACCESS_TOKEN=token`.

Setup a Github webhook on your repo/organization that points to `https://yourserver.herokuapp.com/hooks` with `pull_request` and `issue_comment` feeds. Make sure to set your `SECRET_TOKEN` env variable.

By default, Commodus will look for comments in the open PR for a `LGTM :+1:`