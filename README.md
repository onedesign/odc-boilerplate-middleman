# ODC Middleman Boilerplate

A project boilerplate using the [Middleman](http://middlemanapp.com/) static site generator.

----

## Getting Started


### Initiating a new project...

1. Install Middleman with `gem install middleman`

2. Clone this repository into `~/.middleman/odc-boilerplate-middleman` (you'll have to create this directory if it's not already there).

3. Then you'll be able to use Middleman init with the project template like so: `middleman init my-new-project --template=odc-boilerplate-middleman`


### Middleman Server

To test your site, run `middleman server`, and point your web browser to `http://localhost:4567`

Middleman will process changes to Sass and CoffeeScript files, and if you're lucky it will even refresh your browser when it detects file changes/deletions.


### Building your project

When you're ready to turn your project into a static site, run `middleman build`

This will compile all templates and copy them, along with compiled Sass and CoffeeScript files, over to a `build` directory.


## Using Bourbon...

[Bourbon](http://bourbon.io) is included for CSS vendor prefixing and helpers.


## Adding Scripts…

Middleman uses [Sprockets](https://github.com/sstephenson/sprockets) for importing CoffeeScript/Javascript files. The default for this project uses `#= require_directory .` which will import all files immediately within the `/script` directory (but not files within `vendor` or additional create folders.)

Include new scripts by adding to the top of `/scripts/site.coffee` like so:

`#= require vendor/additional-lib` includes a file called `additional-lib.js` located in `/scripts/vendor/`


## Deployment…

The app can be deployed most easily using [Middleman buildpack from Indirect](https://github.com/indirect/middleman-heroku-static-app), which automatically builds your middleman site directly on heroku at each deploy. From your app directory:

```
# When creating a new app...
heroku create myapp --buildpack http://github.com/indirect/heroku-buildpack-middleman.git

# Or to an existing app...
heroku config:add BUILDPACK_URL=http://github.com/indirect/heroku-buildpack-middleman.git

# And then deploy the app as usual...
git push heroku master
```