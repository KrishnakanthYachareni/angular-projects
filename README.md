
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
