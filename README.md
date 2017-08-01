# Angular2

# Components

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
# Bindings

Coordinates communication between the component's class and its template and often involves passing data.


