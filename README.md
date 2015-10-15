# Dev notes : Commerce Checking
- This is a static site built using Jade
- We are only making the static assets and handing them off to the client

## Stack
- Jade
- Gulp
- Libsass (Indented Sass)
- GitHub

## Gulp build commands

`gulp`

This will compile everything and open the project in the browser for you. It will also watch for changes and refresh the browser on every save.

`gulp ghp`
This is used to copy all the files in the `dist` directory to the `gh-pages` branch for displaying the site.


---

## Environment URLs
- **DEV** - [commercetrust.github.io](http://commercetrust.github.io/checking)


---
## Workflow

### Setup
1. Clone this repo to the local directory of your choice
1. Create a `feature` branch from the `master` branch to work from
1. *You must have Node 4+ installed. [Node](https://nodejs.org/en/) If a version shows up, then you have node installed.*
1. From the project root run `npm i`. This will install all of the node dependencies.
1. Now run `gulp`. This with build the site and launch it in your browser. The site will automatically update with each save of any file.


### Dev deployment
*warning - never merge any branch into `gh-pages`*

1. Push your feature branch `git push origin featureName`
1. Create a pull request to merge into `master`
1. After you merge your feature branch into the `master` branch jump in your terminal and run `gulp ghp`. This will push the changes live to [commercetrust.github.io/checking](http://commercetrust.github.io/checking)

---

### :poop: Clean up
1. Delete your local and remote support ticket branches when done. Avoid leaving stale branches.
1. Local branch removal: run `git branch -d supportBanchName`
1. Remote branch removal: run `git push origin :supportBanchName`
*You can also do this using [SourceTree](http://www.sourcetreeapp.com/) also*


---
## Contacts

### :smiley: Developer(s)
- Benjamin Gandhi-Shepard
- Ryan Trattles

### :smiley: PM(s)
- Jamal McLaughlin


---
### Gulp tasks

Here is a brief explanation of the Gulp tasks


#### PostCSS

[postcss-clearfix](https://github.com/seaneking/postcss-clearfix)

```css
.foo {
  clear: fix; /* IE8+ */
}

.bar {
  clear: fix-legacy; /* IE6+ */
}
```
Compiles to:

```css
.foo:after{
  content: '';
  display: table;
  clear: both;
}

.bar:before,
.bar:after {
  content: '';
  display: table;
}
.bar:after {
  clear: both;
}
.bar {
  zoom: 1;
}
```


[postcss-quantity-queries](https://github.com/pascalduez/postcss-quantity-queries)

```css
ul > li:at-least(4) {
  color: rebeccapurple;
}
```

```css
ul > li:at-most(4) {
  color: rebeccapurple;
}
```

```css
ul > li:between(4, 6) {
  color: rebeccapurple;
}
```

```css
ul > li:exactly(4) {
  color: rebeccapurple;
}
```

---
## Issues that aren't JIRA tickets

### :skull: Known Issues + Workaround Log


---

### :disappointed: Shame Log




### Markdown resources
- [Fast Markdown Tutorial](http://markdowntutorial.com/)
- [GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown/https://help.github.com/articles/github-flavored-markdown/)
- [Markdown Tables](http://www.tablesgenerator.com/markdown_tables)
- :cat: [Available Emojis](https://bitbucket.org/DACOFFEY/wiki/wiki/BITBUCKET/EMOJI/Emoji)
