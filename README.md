# heroku-buildpack-twemproxy

Run [twemproxy](https://github.com/twitter/twemproxy) in a Heroku dyno.

This fork offers the following improvements:

1. twemproxy's timeout is set to 30 seconds to match [Heroku's request timeout](https://devcenter.heroku.com/articles/request-timeout).
1. twemproxy's configuration file is fully rebuilt when the process starts. This permits multiple starts/stops of the process within a running dyno.