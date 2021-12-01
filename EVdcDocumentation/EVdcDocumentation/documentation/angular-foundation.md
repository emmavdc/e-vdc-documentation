# Getting started
## Basic commands
<u>Create angular app</u> :
```
ng new app
```
<u>Create component</u> :
```
ng generate component my-component
```
OR
```
ng g c my-component
```

<u>Create service</u> :
```
ng generate service my-service
```
OR
```
ng g s my-service
```
##Navigation
### RouterLink
```html
<a [routerLink]="['/somewhere']" >Somewhere</a>
```
### Router.Navigate
Example of using with a service :
```javascript
import { Injectable } from '@angular/core';
import {Router} from '@angular/router';

@Injectable({
  providedIn: 'root'
})
export class DatasourceService {

  myMethod(newApplication){  
   ...
    this.router.navigate(['/somewhere']);
  }

  constructor(private readonly router: Router) { }
}
```





