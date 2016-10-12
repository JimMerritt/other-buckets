# Basic Jekyll Build

Jim Merritt's basic Jekyll build. This includes gulp and is based off the build by [Aaron Lasseigne](https://aaronlasseigne.com/2016/02/03/using-gulp-with-jekyll/). Variations have been made to include some extra utility, specifically for using SVG sprites.

### Inclusion of \_site ###
Originally ignored by default for git pushes, the \_site folder is the target of Jekyll's build command. For purposes of a Jekyll build, the folder will be overwritten or recreated if required. When using a series of commands in Gulp, however, this is not as seamless. That has led me to include the base \_site folder in git pushes.
