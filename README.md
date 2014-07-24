polymer-shared-elements
=======================

The idea of this repo is to provide a simple template for a collection of Polymer elements that can be shared between multiple private projects.

The existing toolware (e.g. yo polymer) can generate:

- a private project with its own elements that can live in one github repository
- a public element that lives in its own github repository

I needed somewhere to keep a library of my own elements that I could share between my own projects. I don't particularly want to publish it.

I also wanted to be able to:

- test all my elements with the polymer-test-tools
- use my elements in Polymer Designer

There's nothing fancy here, just a directory structure and a few files. It's crude, but if you need to do the same thing that I do, it may save you a few hours.

To get up and running with the tests, you should just need to clone the repo and run 'bower install'.

### To add an element of your own:

1. duplicate the my-element-template directory and edit according to your needs. Note: metadata.html is what adds your element to the designer palette.
2. add a test to the tests directory 
3. duplicate the htmlsuite function in tests/tests.html
4. add a link to your new element's metadata.html in the root directory's metadata.html

### To add your collection of elements to the Polymer Designer

1. publish your branch to github
2. follow the instructions on the Polymer/designer github page.
