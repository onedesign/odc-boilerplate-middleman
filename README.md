# Project Title Here

Write a one- or two-sentence description of the app, especially if the name of the project doesn't make it completely clear. Example: The portfolio website and CMS for One Design Company.

----

## Getting Started

### Sass setup...

[Sass](http://sass-lang.com/) is an extension of CSS3, adding nested rules, variables, mixins, selector inheritance, and more. It’s translated to well-formatted, standard CSS using the command line tool or a web-framework plugin.

#### ...with the Command Line Tool

1. `gem install sass`
2. `sass --watch styles/site.scss`
3. Sass will be compiled to CSS whenever a file referenced by `site.scss` changes.

#### ...with LiveReload

1. Download [LiveReload](macappstore://itunes.apple.com/app/id482898991?mt=12) from the Mac App Store.
2. Add the project folder to LiveReload.
3. In the project settings, check _Compile SASS, LESS, Stylus, CoffeeScript and others_
4. Sass will be compiled to CSS whenever your project folder changes.

#### ...with CodeKit

1. Download [CodeKit](http://incident57.com/codekit/)
2. Add your project folder to CodeKit
3. Right-click/ctrl-click on site.scss and choose _Set Output Path_
4. Choose the `/styles` directory and click _Select_
5. Sass will be compiled to CSS whenever your project folder changes.

### Adding Bourbon...

[Bourbon](http://thoughtbot.com/bourbon) is a comprehensive library of Sass mixins for all CSS3 properties, providing for support amongst modern browsers. The prefixes also ensure graceful degradation for older browsers that support only CSS3 prefixed properties.

1. `gem install bourbon`
2. In the command line, navigate to `/styles`
3. Add `@import "bourbon/bourbon";` to the very top of `styles/site.scss`
4. Remove `@import "css3-mixins";` from styles/site.scss and delete styles/_css3-mixins.scss from the project.
5. To output properly, Bourbon must be explicitly required (-r) by Sass at the command line: `sass --watch styles/site.scss -r ./styles/bourbon/lib/bourbon.rb`
6. You can update Bourbon in an existing project by navigating to `/styles` and running `bourbon update`

### Adding Compass...

[Compass](http://compass-style.org/) extends Sass with a CSS3 helpers, sprite-generation, typgoraphic rhythm, and more. It can be very useful for large, complicated projects.

1. `gem install compass`
2. `compass create --bare --sass-dir "styles" --css-dir "styles" --javascripts-dir "scripts" --images-dir "images"`
3. Add `@import "compass";` to the very top of `styles/site.scss`
4. Remove `@import "css3-mixins";` from `styles/site.scss` and delete `styles/_css3-mixins.scss` from the project.
3. `compass watch` (Used in place of `sass --watch`)

### Using CoffeScript...

[CoffeeScript](http://coffeescript.org/) is a little language that compiles into JavaScript. Underneath all those awkward braces and semicolons, JavaScript has always had a gorgeous object model at its heart. CoffeeScript is an attempt to expose the good parts of JavaScript in a simple way.

*NOTE:* If you aren't using CoffeeScript for the project, you should delete `scripts/site.coffee` from the project.

#### ...with the Command Line Tool

1. Install [Node.js](http://nodejs.org/) and [npm](https://npmjs.org/)
2. `npm install -g coffee-script` (leave off the `-g` if you don't want to install globally)
3. `coffee --compile scripts/*.coffee` will compile all CoffeeScript to Javascript.
4. `coffee --watch --compile scripts/*.coffee` will compile all CoffeeScript to Javascript whenever a file is saved.

#### ...with LiveReload

1. Download [LiveReload](macappstore://itunes.apple.com/app/id482898991?mt=12) from the Mac App Store.
2. Add the project folder to LiveReload.
3. In the project settings, check _Compile SASS, LESS, Stylus, CoffeeScript and others_
4. CoffeeScript will be compiled to JavaScript whenever your project folder changes.

----

## Gotchas
Take a moment to document corners of the app that might get neglected or present difficulties to newcomers. For example, the [UPitt LessonPlanner](https://github.com/onedesign/LessonPlanner) project calls out the fact that there is an extensive Print Stylesheet that should be maintained as new features are added to the web UI.

----

## Deployment/Releasing
Document the deployment or release process for the app as thoroughly as possible. There's only one thing worse than getting up to speed on a project you've never worked on before, making a bunch of requested changes, and then having no idea how to safely deploy it: that thing is getting asked, after not thinking about said project for months, how to deploy it and having no idea.