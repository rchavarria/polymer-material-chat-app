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

## Building the basic UI structure

We will use `<core-scaffold>` component to scaffold our structure. It comes with
several subcomponents. Take a look at the content of that tag to see it.

`<body fullbleed unresolved>`: `fullbleed` makes the body to fill the viewport.
`unresolved` is used to avoid to display *f*lash *o*f *u*nstyled *c*ontent (FOUC).

Some elements contain `flex` attribute. They expose CSS Flexbox as attributes,
and the child-element under `layout horizontal | vertical` with `flex` attribute takes
up the available space either horizontally or vertically. That means, those
child elements take as much space as they can.

## Using UI elements

Inside the *main content* div we can use a textbox, to write a message, and a button
to send that message.

    <div class="send-message" layout horizontal>
        <paper-input flex label="Type message..." id="input" value="{{input}}"></paper-input>
        <paper-fab icon="send" id="sendButton" on-tap="{{sendMyMessage}}"></paper-fab>
    </div>

Notice the use of double brackets `{{...}}` to reference Polymer data binding and
`on-*` attributes to bind to event handlers.

## Data binding

To activate polymer data binding, just use the tab `<template>`, surrounding the whole
app with this tag we activate it for this app.

Then, we can access to the `{{input}}` variable with this simple code:

``` javascript
var template = document.querySelector('template[is=auto-binding]');
alert(template.input);
```

Repeated elements can be shown this way. In HTML, use the `repeat` attribute of 
`template`

``` html
<template repeat="{{item in items}}">
    <core-item icon="{{item.icon}}" label="{{item.title}}"></core-item>
</template>
```

In JavaScript, define the `items` variable in the template:

``` javascript
template.items = [
    { icon: 'cloud', title: 'My cloud' },
    { icon: 'polymer', title: 'Polymer' },
    { icon: 'favourite', title: 'Love' }
];
```


















