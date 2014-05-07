# UCSP School of Computer Science

Website for the School of Computer Science at UCSP.


# Setup Instructions

The website is based on <http://jekyllrb.com/> Jekyll, based on Ruby.

## Environment setup

**Important**: This guide is oriented for Linux, Unix and Mac OS X 
  systems. For  Windows you are encouraged to use a Ruby bundle, such 
  as RubyInstaller for Windows <http://rubyinstaller.org/>. 


If you already have a Ruby environment configured, proceeed to the
next step.


There are two main methods to have a Ruby environment in your
system. Either using your system packaging tool or rvm. I recomend to
use rvm <http://rvm.io>, since it provides more flexibility when using mutiple Ruby
versions.

This guide will use rvm for Ruby environment setup.

Install RVM and Ruby:

`\curl -sSL https://get.rvm.io | bash -s stable --ruby`

Follow screen instructions. Make sure you do 
`source $HOME/.rvm/scripts/rvm` to have the Ruby rvm environment
loaded in your session. 


## Jekyll setup

Install Jekyll gem.
`gem install jekyll`

# Getting sources

Clone the git repository
`git clone https://github.com/cs-ucsp/cs-ucsp.git`

Start hacking!

# Project organization and contributing

The project uses the Bootstrap <http://getbootstrap.com/> front-end
framework.

* _layouts/ - contains website layout (general template)
* css/ - contains custom and Bootstrap' CSS stylesheets
* fonts/ - contains webfonts
* img/ - contains images
* js/ - contains custom and Bootstrap' Javascript
* _posts/ - Ignore this directory by now :)
* _config.yml - Jekyll configuration

## Creating new pages / sections

To create a new page you will need to create a new Jekyll-compatible
HTML file. For instance, if you create a file named `newfile.html` the
content of such file will be shown in the URI
<http://cs.ucsp.edu.pe/newfile.html>. 

if you want to create a section or area, you will need to create a
directory and place at least a `index.html` Jekyll-compatible HTML
inside. For instance, if you want to create a section named
`publications`, create a `publications` directory. It will be shown in
the URI <http://cs.ucsp.edu.pe/publications/>

## Testing changes

To test your changes, run `jekyll serve`. It will launch a webserver
on <http://localhost:4000>. Enter that address in your browser and you
are set.

You can also use `jekyll server -w` to make jekyll watch for changes
and regenerate the static HTML.

# Controlling the project (REDMINE)

We use Redmine to manage the tasks that need to be done for this project.

For contributing you need to:
 - Go to the Project on Redmine: http://cs.ucsp.edu.pe/projects/projects/cs-www
 - Go to the Issues tab (http://cs.ucsp.edu.pe/projects/projects/cs-www/issues)
 - Select the issue you want to solve 
 (only the ones with status `New`, `In Progress` and `Feedback`)
 - When you think the issue is solved, change its Status to `Resolved` and 
 assign it to *Raul Gallegos* or *Rudy Godoy*.
 - If you think that there should be more issues that are not listed there, go
 ahead and create it, and assign *Raul Gallegos* or *Rudy Godoy* as watchers.

If you don't have an account, ask directly one, and we'll create and email it
 back to you.


## How to contribute:

For those issues that need to change the site code (including html, script, docs, 
etc.), you need to use branches, go to the project root and create a new branch 
for the specific issue you are solving, for example for the issue #123:

    git checkout -b ticket-123

Then make your changes, commit them and then push it back to origin (github).
Then on the github project page, create a new Pull Request with the branch you 
created; We will make sure that the contribution is correct and merge it with 
the master branch.

You can learn more about Pull Requests here: <https://help.github.com/articles/creating-a-pull-request>.
