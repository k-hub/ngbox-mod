# ngbox-mod

Stripped dependencies from https://github.com/mixalistzikas/ngbox and a few bug fixes.

Added custom CSS to component and modified directive to work with dynamic templates with img and/or video tags. 

# Install npm package directly into your angular project
- cd to the project you want to use this module in
- `npm install https://github.com/k-hub/ngbox.git`

# app.module.ts
Add the following imports to your app.module.ts

`import { NgBoxModule } from 'ngbox/ngbox.module';`

`import { NgBoxService } from 'ngbox/ngbox.service';`

`import { CommonModule } from '@angular/common';`

`Add to imports NgBoxModule, BrowserModule, CommonModule`

Add to services `NgBoxService`

# app.component.html
Add this at the top `<ngbox></ngbox>` of your root html file.

# tsconfig.json
Add `"include": [ "node_modules/ngbox/**/*.ts", "src/**/*.ts" ]`

# ngBox
Add `ng-box` to your img or video tags. The required param is src.

Attributes
`src` (The source file/video as a string)

`[src]` (The source file/video as a variable)

`group="myGroup"` (grouping as a string)

`[group]="group"` (grouping as a variable)

`[image]="true"` (if the path or the source has .jpg or .png it will open automatically, if not then you need to specify that this source is an image)

`[width]="800" [height]="800"`

`[title]="This is a title"`

`[cache]="true"` (if you want to preload an image)
