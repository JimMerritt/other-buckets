# Basic Jekyll Build

Jim Merritt's basic Jekyll build. This includes gulp and is based off the build by [Aaron Lasseigne](https://aaronlasseigne.com/2016/02/03/using-gulp-with-jekyll/). Variations have been made to include some extra utility, specifically for using SVG sprites.

### Inclusion of \_site ###
Originally ignored by default for git pushes, the \_site folder is the target of Jekyll's build command. For purposes of a Jekyll build, the folder will be overwritten or recreated if required. When using a series of commands in Gulp, however, this is not as seamless. That has led me to include the base \_site folder in git pushes.

### This is an overall hub for quick dev.
Using this as a go-to spot for a standard build to allow quick iteration of concepts.

## Tools
I'm using gulp to increase efficiency when building. The main purpose is for CSS/SASS and JavaScript concatenation and minification as well as using the JavaScript Babel tool to assure ES6 fallbacks and to improve code reliability.

### Addon List
- gulp
- gulp-util
- gulp-concat
- gulp-sass
- gulp-sass-glob
- child_process
- browser-sync
- gulp-autoprefixer
- gulp-cssnano
- gulp-svgstore
- gulp-svgmin
- gulp-cheerio
- path
- babel

## Adding Production Environment
When setting a 'production environment' only asset or variable, a Gulp task is established to run as 'Production Environment'. To conditionally include assets or variables into the build during this time, set within a liquid template conditional tag.

```
{% if jekyll.environment == 'production' %}
  // Include assets here
{% endif %}
```

Then, when producing, run 'gulp  produce' to output a production build. This was originally built as an easy solution for Google Analytics code to not run on the local build.
