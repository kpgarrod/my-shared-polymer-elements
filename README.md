polymer-shared-elements
=======================

The idea of this repo is to provide a simple template for a collection of Polymer elements that can be shared between multiple private projects.

The existing toolware (e.g. yo polymer) can generate:

- a private project with its own elements that can live in one github repository
- a public element that lives in its own github repository

I needed somewhere to keep a library of my own elements that I could share between my own projects. I don't particularly want to publish it and I didn't want to keep each element in it's own private repository.

I also wanted to be able to:

- test all my elements with the polymer-test-tools
- use my elements in Polymer Designer

There's nothing fancy here, just a directory structure and a few files. It's crude, but if you need to do the same thing that I do, it may save you a couple of hours.

### To get up and running with the tests:

1. clone the repo
2. run 'bower install'
3. start a server in the root directory
4. point your browser at runner.html
5. there's no Karma, so you may want to use livereload to refresh the page

### To add a new element and test of your own:

1. duplicate the my-element-template directory and edit according to your needs. Note: metadata.html is what adds your element to the designer palette.
2. add a test to the tests directory by duplicating my-element-template.test.html 
3. duplicate the htmlsuite function in tests/tests.html and point it to your test from 2. above
4. duplicate the link in the root directory's metadata.html and point the link at the metadata.html file from 1. above  

### To add your collection of elements to the Polymer Designer Palette

1. publish your branch to github
2. follow the instructions under <strong>Adding your own components to designer</strong> on the Polymer/designer github page
