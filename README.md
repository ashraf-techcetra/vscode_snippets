# VScode User Snippets 
---
## Handlebars
|prefix|stands for|Description
---|---|---
[fl](#fl)|form layout|Extract `form` with `.form-layout` div. Which is parent for our set on `.form-rows`.
[flr](#flr)|form layout row |Extract div with `.form-row` class. Use to create row in `.form-layout`
[flf](#flf)|form layout field|Extract div with `.form-field` class use for create column in `.form-row`
[flrf](#flrf)|form layout with row and field| Extract one row with one column div structure.

### fl (form layout)
```html
<form action='' method='post' class='check-form'>
  <div class='form-layout'>
    ...
  </div>
</form>
```

### flr (form layout row)
```html
<div class='form-row'>
  ...
</div>
```

### flf (form layout field)
```html
<div class='form-field'>
  ...
</div>
```
### flrf (form layout with row and field)
```html
<div class='form-row'>
  <div class='form-field'>
    ...
  </div>
</div>
```

