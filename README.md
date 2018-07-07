
## Angular Installation

1. Node Js (Path automatically sets)
2. Install Typescript 
```npm install -g typescript```
3. Download bootstrap(Unzip it) and then copy ```bootstrap.css``` file into your angular appliucation ```/app-name``` folder after that edit ```angular.json or angular-cli.json``` file
```
"styles": [
              "src/styles.css",
              "src/bootstrap.css"
            ],
```
4. Install Angular Cli
```npm install  -g @angular/cli```
5. Install Visual Studio Code / Atom IDE. and then
Install the following extentions in Visual Studio Code
```angular-cli, angular v4 snippets, debugger for chrome, tslint, typescript importer. ```

## Directives
Directives have ```@Directive``` attribute or one of its subclasses. We have three primary types.
1. **Components**
2. **Structural dirctives**(*ngFor, *ngIf)
3. **Attribute directives**(ngModel)

## Component
 Components are a logical piece of code for Angular JS application.A Component consists of the following
1. **Template:** 
This is used to render the view for the application. This contains the HTML that needs to be rendered in the application. 
This part also includes the binding and directives.
2. **Class:** This is like a class defined in any language such as C. This contains properties and methods. 
This has the code which is used to support the view. It is defined in TypeScript.
3. **MetaData:** 
This has the extra data defined for the Angular class. It is defined with a decorator.To create the component
```
ng generate component folder/component-name or only component-name
```
or with shortcuts
```
ng g c folder/component-name or only component-name
```
### ngFor
NgFor is a structural directive, meaning that it changes the structure of the DOM.
It’s point is to repeat a given HTML template once for each value in an array, each time passing it the array value as context for string interpolation or binding.
```
@Component({
  selector: 'ngfor-example',
  template: `
 <ul>
  <li *ngFor="let person of people"> 
    {{ person.name }}
  </li>
 </ul>
 `
})
class NgForExampleComponent {
  people: any[] = [
    {
      "name": "Krishnakanth  Yachareni"
    },
    {
      "name": "Srikanth  Yachareni"
    }
  ];
}
```
### ngModel
The ```ngModel``` directive binds an input,select, textarea (or custom form control) to a property on the scope using NgModelController, which is created and exposed by this directive. ```ngModel``` is responsible for:
* Binding the view into the model, which other directives such as input, textarea or select require.
* Providing validation behavior (i.e. required, number, email, url).
* Keeping the state of the control (valid/invalid, dirty/pristine, touched/untouched, validation errors).
* Setting related css classes on the element (ng-valid, ng-invalid, ng-dirty, ng-pristine, ng-touched, ng-untouched, ng-empty, ng-not-empty) including animations.
* Registering the control with its parent form.
```
import {Component} from '@angular/core';
 
@Component({
  selector: 'example-app',
  template: `
    <input [(ngModel)]="name" #ctrl="ngModel" required>
 
    <p>Value: {{ name }}</p>
    <p>Valid: {{ ctrl.valid }}</p>
    
    <button (click)="setValue()">Set value</button>
  `,
})
export class SimpleNgModelComp {
  name: string = '';
 
  setValue() { this.name = 'Krishnaknth'; }
}
```
