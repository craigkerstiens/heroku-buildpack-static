Heroku buildpack: Static
========================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpack) for static apps. 
It uses Apache to statically serve your content. It also supports securely serving your static content.
To securely serve your content you need to set two variables:

    heroku config:add USERNAME=usernamehere
    heroku config:add PASSWORD=passwordhere


Usage
-----

Example usage:

    $ cat 'hello world' > index.html

    $ heroku create --stack cedar --buildpack git@github.com:craigkerstiens/heroku-buildpack-static.git

    $ git push heroku master
    ...

The buildpack will detect your app as Static if it has the file `index.html` in the root. 
