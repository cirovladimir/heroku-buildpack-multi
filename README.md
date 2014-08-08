# heroku-buildpack-multi

Use multiple buildpacks on your app

## Usage

    $ heroku config:add BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi.git

    $ cat .buildpacks
    https://github.com/heroku/heroku-buildpack-nodejs.git#0198c71daa8
    https://github.com/heroku/heroku-buildpack-ruby.git#v86

## Base path for each buildpack

If you have a nested application, i.e. you have a java app for the backend and your client app (frontend) inside src/main/webapp, you could add the basepath right after each buildpack

    $ cat .buildpacks
    https://github.com/heroku/heroku-buildpack-java
    https://github.com/heroku/heroku-buildpack-nodejs#v60	src/main/webapp