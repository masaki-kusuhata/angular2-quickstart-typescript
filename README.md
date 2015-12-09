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
npm i systemjs typescript
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

### make app.ts

```javascript
import {bootstrap, Component} from 'angular2/angular2';
@Component({
    selector: 'my-app',
    template: '<h1>My First Angular 2 App</h1>'
})
class AppComponent { }
bootstrap(AppComponent);
```

### make index.html

```html
<html>
  <head>
    <title>Angular 2 QuickStart</title>
    <script src="node_modules/systemjs/dist/system.js"></script>
    <script src="node_modules/typescript/lib/typescript.js"></script>
    <script src="node_modules/angular2/bundles/angular2.dev.js"></script>
    <script>
      System.config({
        transpiler: 'typescript',
        typescriptOptions: { emitDecoratorMetadata: true }
      });
      System.import('./app.ts');
    </script>
  </head>
  <body>
    <my-app>loading...</my-app>
  </body>
</html>

```

### run

```bash
npm start
```

https://angular.io/docs/ts/latest/quickstart.html
