# Angular2 - Codemirror component

Typescript version of https://github.com/chymz/ng2-codemirror

### <a name="install"></a>Installation

- Include Codemirror javascript files in your application (with files for modes)
- Install ng2-codemirror-typescript
  - NPM : `npm install ng2-codemirror-typescript`

### <a name="dependencies"></a>Dependencies
CodeMirror library is required for this component :
  - Install via NPM : `npm install codemirror`

CodeMirror need to be accessible by `import 'codemirror'`

Then you need to include base CSS of codemirror located in `codemirror/lib/codemirror.css`

Pay attention, if you want to use placeholder you need to import `codemirror/addon/display/placeholder.js`

### <a name="sample"></a>Sample (ES2016+)

Include `CodemirrorModule` in your main module :

```javascript
import {CodemirrorModule} from 'ng2-codemirror/Codemirror';

@NgModule({
  // ...
  imports:      [
    CodemirrorModule
  ],
  // ...
})
export class AppModule { }
```

```javascript
import {Component} from 'angular2/core';

@Component({
  selector: 'sample',
  template: `<codemirror [(ngModel)]="code" [config]="{...}" placeholder="Here is the code placeholder"></codemirror>`
})
export class Sample{
  constructor(){
    this.code = `// Some code...`;
  }
}
```
