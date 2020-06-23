
# Sass Cheat Sheet

### Preprocessing
```bash
# auto-preprocess
sass --watch input.scss output.css
```
```bash
# output to a specific directory
sass --watch app/sass:public/stylesheets
```

### Syntax
```sass
// basic variable and class declaration
$font-stack:    Helvetica, sans-serif
$primary-color: #333

body
  font: 100% $font-stack
  color: $primary-color
  
  ul
    margin: 0
    padding: 0
    list-style: none
    
// mixins
=transform($property)
  -webkit-transform: $property
  -ms-transform: $property
  transform: $property
.box
  +transform(rotate(30deg))
  
// extends
%message-shared
  border: 1px solid #ccc
  padding: 10px
  color: #333

.success
  @extend %message-shared
  border-color: green
  
// operators
article[role="main"]
  float: left
  width: 600px / 960px * 100%
```
