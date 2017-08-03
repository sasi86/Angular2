# Angular2

## Components

Components = Template + [class = properties + Method] + Metadata

```javascript
import { Component, OnInit } from '@angular/core';

@Component({
    module: module.Id, // to mention relative path in templateUrl and styleUrl
    selector: 'selector-name',
    template: `` || "" //backticks supports multiline templating where double quotes doesn't
    templateUrl: 'name.component.html',
    style: '',
    styleUrl: 'name.css'
})

export class NameComponent implements OnInit {
    constructor() { }
    ngOnInit() { }
}
```
## Bindings

Coordinates communication between the component's class and its template and often involves passing data.

### Interpolation - oneway binding - without quotes

{{template_expression}}

ex: {{pageTitle}}

### Event Bindings 

<button (click)= 'toggleImage()'>

List of events : https://developer.mozilla.org/en-US/docs/Web/Events

### Twoway Binding

[(ngmodel)]='expression'

ngModel directive is part of FormsModule. FormModule need to be imported to the appmodule. Do the following

```javascript
import { FormsModule} from '@angular/forms'

@NgModule({
import: [FormsModule],
declarations: [...],
providers: [...],
bootstrap:[AppComponent]
})
export class AppModule{}
```

# Property Bindings

list of properties that could be bind is found @ https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes

# Directives 

1. Custom Directive - Component as a directives
2. Builtin directive - Structural Directive found in BrowserModule
*ngIf='expression'
*ngFor='let ... of ...'

# Pipes 

Transforms bound properties before display.

Built-in pipes : date,number,currency,percent,decimal,json,slice,lowercase,uppercase ....

Chaining pipes : {{product.price | currency | lowercase}}
pipes with Parameters : {{ product.price | currency : 'USD' : true : '1.2-2'
- currency code
- display currency symbol
- min # of integer digits, min # decimal digits, max # of decimal digits

Custom Pipes : 



