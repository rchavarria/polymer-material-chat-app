# polymer-material-chat-app

A chat application made in Polymer using material desing, just for learning

It's been inspired in this tutorial : http://www.pubnub.com/blog/creating-a-polymer-chat-app-with-material-design/

# Prerequisites

- Install node
- Install bower

Don't forget to run `bower install` before any new installation.

# Steps

## Init node app

    npm init

## Install Polymer

    npm install --save Polymer/polymer

## Import polymer webcomponents

    <script src="bower_components/webcomponentsjs/webcomponents.min.js"></script>

## Import some core and paper elements

    $ bower install Polymer/core-scaffold
    $ bower install Polymer/core-item
    $ bower install Polymer/paper-input
    $ bower install Polymer/paper-fab

## Import those documents in your index.html page

    <link rel="import" href="bower_components/core-scaffold/core-scaffold.html">
    <link rel="import" href="bower_components/core-item/core-item.html">
    <link rel="import" href="bower_components/paper-input/paper-input.html">
    <link rel="import" href="bower_components/paper-fab/paper-fab.html">

## CONTINUE WITH STEP 1.3
