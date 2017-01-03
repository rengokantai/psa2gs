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
###5 Transforming Data with Pipes
####03:31
```
{{product.price|currency:'USD':true:'1.2-2'}}
```
##7. More on Components
###2 Defining Interfaces
vscode: do not show certain files  
in settings.json
```
{
  "files.exclude":{
    "**/app/**/*.js":true,
    "**/*.map":true,
  }
}
```
###6 Relative Paths with Module Id
we can use relative path(s)
```
@Component({
  moduleId:module.id,
  templateUrl:'product-list.component.html',
  styleUrls:['product-list.component.css']
})
```
##8. Building Nested Components
###3 Using a Nested Component
```
import {Component,OnChanges} from '@angular/core';
export class StarComponent implement OnChanges{
  ngOnChanges():void{
    this.starWidth = this.rating*86/5;
  }
}
```
###4 Passing Data to a Nested Component Using @Input
passing data from container component to child component.
put property in template
```
<ai-star  [rating]="">
```
put @Input in child component
```
@Component({
  selector:'ai-star',
  templateUrl:''
})
export class StarComponent{
  @Input() rating:number;
  starWidth:number;
}
```
###5 Passing Data from a Component Using @Output
passing data from child to container component.
```
@Output() notify:EventEmitter<string> = new EventEmitter<string>();
onClick(){
  this.notify.emit('clicked');
}
```


##9. Services and Dependency Injection

##11. Navigation and Routing Basics
###3 Configuring Routes
app.module.ts
```
import { RouterModule } from '@angular/router';
@NgModule({
  imports:[
    BrowserModule,
    FormsModule,
    HttpModule,
    ROuterModule.forRoot([])
  ],
  declarations:[
  ]
})
```

