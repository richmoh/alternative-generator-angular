# Module based AngularJS generator

> An alternative module based Yeoman generator for AngularJS - Forked from https://github.com/yeoman/generator-angular

## Usage

It's early days yet so nothing super easy and fancy I'm afraid. To install do the following....

`git clone git@github.com:richmoh/generator-modular-angular.git`

`cd generator-modular-angular`

`npm link`

The generator should then be installed (this has only been tested on Mac)

To create a new project using the generator: 

`mkdir {dir name}`

`cd {dir name}`

`yo modular-angular {app name}`

Follow the prompts and done!

## Generator

To create a new "module" - for now thats the controller, service, view and routes to go with it run...

`yo modular-angular:module {route}`

This will create a module with following file structure:

`/modules/{route}/service.js
/modules/{route}/controller.js
/modules/{route}/view.html`

and add the following to the app.js file: 

`.when('/{route}', {
        templateUrl: 'modules/{route}/view.html',
        controller: '{route}Ctrl'
      }) // {route} would be replaced with the route entered`

If you don't like this file structure I recommend using: https://github.com/yeoman/generator-angular instead ;)
