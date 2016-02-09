# The Two Smart Guys Learning Project
Here's how we develop:

* [git](git-scm.com) for source code control, and [Github](gihub.com) to share source and documentation
* [Atom](aton.io) as a code editor
* [Ruby on Rails](http://rubyonrails.org/) for the backend, and simple front-end
* [Bootstrap](http://getbootstrap.com/) for responsive layouts, meaning they adapt to the size and type of the display device
* [React](https://facebook.github.io/react/) for fast, easy to understand, browser-side code

## Installing Git
Here are the instructions for installing git: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git. This is for the command line tools that run on your computer. They work with repositories on your computer, and remote repositories, like those on Github. Git is open source software, and is free.

Here's how to get started on Github: https://help.github.com/articles/set-up-git/. Github provides remote, shareable source code control repositories, and a way to create web sites for projects. It's free to use Github if you're willing to share your project publicly.

## Installing Atom
Links to installers are on the Atom home page: https://atom.io/.

Once you install Atom, start it. You can type `atom .` at a command prompt. Atom will start on the current directory, and put itself in the background. 

Type "Ctrl-Shift-p" to get the list of all commands, and type "settings". Click on the "Settings View: Open" line. Or, instead of all that, just type "Ctrl-,". Either way, then click on "Packages", then install the following packages:

* Sublime-Style-Column-Selection
* atom-beautify
* javascript-snippets
* language-javascript-jsx
* linter
* react
* language-rails

## Installing Ruby on Rails
Since Rails 5 is about to come out, we're going to install Rails 5 beta 2. First, you need to install Ruby version 2.3.0 or higher, which includes the Rubygems packaging system for downloading other people's packages. You also need SQLite3.

### Installing Ruby
There is a Windows and Mac installer at http://railsinstaller.org/. However, this doesn't install the Rails 5 beta.

### Installing SQLite3
According to the Rails guides, "Many popular UNIX-like OSes ship with an acceptable version of SQLite3." The installers for Windows are on this page: https://www.sqlite.org/download.html.

## Bootstrap
Bootstrap is a combination of CSS and JavaScript that helps lay out pages, and makes it easy to define layouts that adapt to the size of the display device (e.g. desktop big screen, smartphone, or tablet). There are ways to download and install it so you host it yourself on your web site, but we'll start by using versions hosted on a content delivery network (CDN).

```
<!-- Latest compiled and minified CSS -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" integrity="sha384-1q8mTJOASx8j1Au+a5WDVnPi2lkFfwwEAa8hDDdjZlpLegxhjVME1fgjWPGmkzs7" crossorigin="anonymous">

<!-- Optional theme -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap-theme.min.css" integrity="sha384-fLW2N01lMqjakBkx3l/M9EahuwpSfeNvV63J5ezn3uZzapT0u7EYsXMjQV+0En5r" crossorigin="anonymous">

<!-- Latest compiled and minified JavaScript -->
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js" integrity="sha384-0mSbJDEHialfmuBBQP6A4Qrprq5OVfW37PRR3j5ELqxss1yVqOtnepnHVP9aJ7xS" crossorigin="anonymous"></script>
```

## React
React is a framework from Facebook for writing the view part of web pages, especially for single-page or very reactive browser side applications. Like Bootstrap, you can install it on your web site to be served to your users, but we'll start by using a version hosted at Facebook.

```
<script src="https://fb.me/react-0.14.7.js"></script>
<script src="https://fb.me/react-dom-0.14.7.js"></script>
```

## How the pieces fit together
The "Github model" is like this: There is a remote repository for the project. One or more people are allowed to commit directly to the respository on Github. Other contributors fork the project and work on their own repository. When they're finished with their changes, the send a pull request to a commiter, who reviews the work and merges it into the project repository if the pull request is wanted.

Rails provides a full model-view-controller framework for developing web applications. The model part provides a complete object-relational mapping component (ORM), that makes it relatively easy to develop against a local copy of a light-weight RDBMS like SQLite3, then deploy to production against MySQL or, the current favourite among the cool kids, Postgres.

The view component provides a template completion framework so that the HTML can be generated on the fly based on Ruby code.

The controller component manages combining the models with the views.

React is a JavaScript based language that makes it easier to write web pages by combining simple React modules into more complicated modules in a relatively easy to understand way. React code is compiled to JavaScript (the cool kids call it "transpiling"), which is what runs in the browser.

Rails also comes with support for newer-style, single-page apps. The controller can generate JSON (or XML) instead of HTML, to be fed to a React front end, for example. With optional gems, Rails can manage the transpiling of the React code.

Bootstrap defines CSS classes that you can attach to your HTML elements. When the page is rendered, Bootstrap will lay out your page intelligently.
