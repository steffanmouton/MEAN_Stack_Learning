# Learning Angular

### NG CLI Basics
##### CLI Commands:
| Command | Functionality |
|---|---|
| npm install -g @angular cli | initial install of the angular system |
| ng new app-name | generates a new application with the name app-name |
| ng serve | begins hosting the application |
| ng g c | generates a new component |
|  |  |

### Angular Basics

##### If getting powershell permission error in IDE:
Run ```Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser``` in terminal.

##### Loading flow:
index.html will be loaded on page first > loads main.ts > loads the main app component. 
app.module.ts contains the instructions for the module. the bootstrap array is where you define what components must be loaded immediately. 

##### When creating a new Component:
1. Create a new folder for the component, under the app folder. Create files there with name convention _component-name_.component.html and _component-name_.component.ts
2. Lay down boilerplate for the .ts file:
```ts
import { Component } from '@angular/core';

@Component({
    selector: 'app-server',
    templateUrl: './server.component.html'
})
export class ServerComponent
{

}
```
3. Register the new component in the app.module.ts file by adding it to the declarations array in the NgModule decorator. Also, add the import statement at the top of the file.

##### Styling:
In name.component.ts, in component declaration:
styleUrls - array


##### Misc.  

All Components MUST have a template or templateUrl declared.  

---  

Calling a component (e.g. "app-servers") to display can be done in many ways:  

```html
<app-servers></app-servers>
<div app-servers></div>
<div class="app-servers"></div>
```
    
All of these would work, but the first is the preferred for components.  

---
