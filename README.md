# ODC Middleman Boilerplate

A project boilerplate using the [Middleman](http://middlemanapp.com/) static site generator.

----

## Getting Started

### Initiating a new project...

Install Middleman with `gem install middleman`

Clone this repository into `~/.middleman/odc-boilerplate-middleman` (you'll have to create this directory if it's not already there).

Then you'll be able to use Middleman init with the project template like so: `middleman init my-new-project --template=odc-boilerplate-middleman`

### Middleman Server

To test your site, run `middleman server`, and point your web browser to `http://localhost:4567`

Middleman will process changes to Sass and CoffeeScript files, and if you're lucky it will even refresh your browser when it detects file changes/deletions.

### Building your project

When you're ready to turn your project into a static site, run `middleman build`

This will compile all templates and copy them, along with compiled Sass and CoffeeScript files, over to a `build` directory.