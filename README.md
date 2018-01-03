# VScode User Snippets 
---
## Handlebars
|prefix|stands for|Description
---|---|---
[fl](#fl-form-layout)|form layout|Extract `form` with `.form-layout` div. Which is parent for our set on `.form-rows`.
[flr](#flr-form-layout-row)|form layout row |Extract div with `.form-row` class. Use to create row in `.form-layout`
[flf](#flf-form-layout-field)|form layout field|Extract div with `.form-field` class use for create column in `.form-row`
[flrf](#flrf-form-layout-with-row-and-field)|form layout with row and field| Extract one row with one column div structure.
[pr](#pr-partial)|Partial|Extract basic partials tag.
[prl](#prl-partial-from-layout-folder)|partial from layout folder|Extract basic partials with list file name from `layout` folder
[prm](#prm-partial-from-modules-folder)|partial from modules folder|Extract basic partials with list file name from `modules` folder
[prmfe](#prmfe-partial-modules-error)|partial modules error|Extract error partials from `modules/form` file
[prmfi](#prmfi-partial-modules-form-input)|partial modules form input|Extract input partials from `modules/form` file


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
### pr (partial)
```hbs
{{> /path/to/partials
  partials options
}}
```
### prl (partial from layout folder)
```hbs
{{> layout/(head|header|footer|nav)
  partials options
}}
```
### prm (partial from  modules folder)
```hbs
{{> layout/(breadcrumbs|component|form|icons|loader|select|overla/open|overlay/close)
  partials options
}}
```

### prmfe (partial modules error)
```hbs
  {{> modules/form field_type='errors' errors=errors_arrary }}
```

### prmfi (partial modules form input)
```hbs
{{> modules/form field_type='input'
  type='text'
  name='first_name'
  class='first-name'
  placeholder='eg. Jhon Doe'
  id='first_name'
}}
```
