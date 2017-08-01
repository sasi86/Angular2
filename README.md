# Angular2

# Components

Components = Template + [class = properties + Method] + Metadata

import { Component, OnInit } from '@angular/core';

@Component({
    selector: 'selector-name',
    templateUrl: 'name.component.html'
})

export class NameComponent implements OnInit {
    constructor() { }

    ngOnInit() { }
}
