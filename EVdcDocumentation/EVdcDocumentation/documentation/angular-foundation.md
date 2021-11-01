# Getting started
## Basic commands
<u>Init</u> :
```
ng new my-app
```
<u>Component</u> :
```
ng generate component my-component
```
<u>Service</u> :
```
ng generate service my-service
```
##Navigation
### RouterLink
```html
<li>
  <a [routerLink]="['/gallery']" >Gallery</a>
</li>
```
### Router.Navigate
Example of using with a service :
```javascript
import { Injectable } from '@angular/core';
import {Router} from '@angular/router';
import { Environment } from '../models/environment';

@Injectable({
  providedIn: 'root'
})
export class DatasourceService {

  applicationEnv : Environment;

  initApplication(newApplication){
    this.applicationEnv = newApplication;
    let i = 1;
    for (const config of this.applicationEnv.configurations) {
      config.configurationId = i;
      i++;
    }
    this.router.navigate(['/validation/local-application'])
  }

  constructor(private readonly router: Router) { }
}
```





