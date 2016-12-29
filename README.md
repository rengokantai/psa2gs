# psa2gs
##5. Templates, Interpolation, and Directives
###2 Building a Template
```
templateUrl:'a-list.component.html'
```
###4 Using a Component as a Directive
add components in app.module.ts
```
import {NgModule} from '@angular/core';
@NgModule({
  imports:[],
  declarations:[
    AppComponent,
    ProductListComponent
  ]
})
```


##6. Data Binding & Pipes
###4 Handling Input with Two-way Binding
```
import {NgModule} from '@angular/core';
import {FormModule} from '@angular/forms';
@NgModule({
  imports:[
    BrowserModule,
    FormsModule
  ]
})
```
