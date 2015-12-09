# angular2-quickstart-javascript

### Create a project folder

```bash
mkdir angular2-quickstart
cd angular2-quickstart
```

### Install essential libraries

```bash
npm init -y
npm i angular2@2.0.0-alpha.44 --save --save-exact
npm i live-server --save-dev
```

change package.json:

```
{
  "scripts": {
    "start": "live-server"
  }
}
```

### make app.js

```javascript
(function() {
var AppComponent = ng
  .Component({
    selector: 'my-app',
    template: '<h1>My First Angular 2 App</h1>'
  })
  .Class({
    constructor: function () { }
  });
document.addEventListener('DOMContentLoaded', function() {
  ng.bootstrap(AppComponent);
});
})();
```

### make index.html

```html
<html>
  <head>
    <title>Angular 2 QuickStart</title>
    <script src="node_modules/angular2/bundles/angular2.sfx.dev.js"></script>
    <script src="app.js"></script>
  </head>
  <body>
    <my-app></my-app>
  </body>
</html>
```

### run

```bash
npm start
```

https://angular.io/docs/ts/latest/quickstart.html
