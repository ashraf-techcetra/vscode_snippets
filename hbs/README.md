# VScode User Snippets 
---
## Handlebars
### hbs and html basic
|Prefix|Stands for|Description
---|---|---
[fl](#fl-form-layout)|form layout|Extract `form` with `.form-layout` div. Which is parent for our set on `.form-rows`.
[flr](#flr-form-layout-row)|form layout row |Extract div with `.form-row` class. Use to create row in `.form-layout`
[flf](#flf-form-layout-field)|form layout field|Extract div with `.form-field` class use for create column in `.form-row`
[flrf](#flrf-form-layout-with-row-and-field)|form layout with row and field| Extract one row with one column div structure.
---
### hbs partials
|Prefix|Stands for|Description
---|---|---
[pr](#pr-partial)|Partial|Extract basic partials tag.
[prl](#prl-partial-from-layout-folder)|partial from layout folder|Extract basic partials with list file name from `layout` folder
[prm](#prm-partial-from-modules-folder)|partial from modules folder|Extract basic partials with list file name from `modules` folder
---
### hbs form partials
|Prefix|Stands for|Description
---|---|---
[prmfe](#prmfe-partial-modules-form-error)|partial modules form error|Extract error partials from `modules/form` file
[prmfi](#prmfi-partial-modules-form-input)|partial modules form input|Extract `input` partials from `modules/form` file
[prmfir](#prmfir-partial-modules-form-input-radio)|partial modules form input radio | Extract input `input[type="radio"]` partials from `modules/form` file
[prmfic](#prmfic-partial-modules-form-input-checkbox)|partial modules form input checkbox | Extract `input[type="checkbox"]` partials from `modules/form` file
[prmfif](#prmfif-partial-modules-form-input-file)|partial modules form input file | Extract `input[type="file"]` partials from `modules/form` file
[prmft](#prmft-partials-modules-form-textarea)|partial modules form textarea| Extract textarea partials from `modules/form` file
---
### hbs form field partials
|Prefix|Stands for|Description
---|---|---
[prmffi](#prmffi-partial-modules-form-field-input)|partial modules form field input | Extract [input](#prmfi-partial-modules-form-input) inside [form-field](#flf-form-layout-field)
[prmffca](#prmffi-partial-modules-form-field-checkbox-array)|partial modules form field checkbox array | Extract [input](#prmfi-partial-modules-form-input-checkbox) inside [form-field](#flf-form-layout-field) with array
[prmffco](#prmffi-partial-modules-form-field-checkbox-object)|partial modules form field checkbox object | Extract [input](#prmfi-partial-modules-form-input-checkbox) inside [form-field](#flf-form-layout-field) with object
[prmffra](#prmffi-partial-modules-form-field-radio-array)|partial modules form field radio array | Extract [input](#prmfi-partial-modules-form-input-radio) inside [form-field](#flf-form-layout-field) with array
[prmffro](#prmffi-partial-modules-form-field-radio-object)|partial modules form field radio object | Extract [input](#prmfi-partial-modules-form-input-radio) inside [form-field](#flf-form-layout-field) with object
[prmffa](#prmffa-partial-modules-form-field-addon)|partial modules form field addon | Extract [input](#prmfi-partial-modules-form-input) with addon text inside [form-field](#flf-form-layout-field)
[prmffd](#prmffd-partial-modules-form-field-datepicker)|partial modules form field datepicker | Extract [input](#prmfi-partial-modules-form-input) with calender icon, inside [form-field](#flf-form-layout-field)
[prmfftp](#prmfftp-partial-modules-form-field-timepicker)|partial modules form field timepicker | Extract [input](#prmfi-partial-modules-form-input) with time icon, inside [form-field](#flf-form-layout-field)
[prmfff](#prmfff-partial-modules-form-field-file)|partial modules form field file | Extract [input-file](#prmfif-partial-modules-form-input-file) inside [form-field](#flf-form-layout-field)
[prmffs](#prmffs-partial-modules-form-field-select)|partial modules form field select | Extract select with respoctive parse `object` or `arrary` inside [form-field](#flf-form-layout-field)
[prmfft](#prmfft-partial-modules-form-field-textarea)|partial modules form field textarea | Extract [textarea](#prmft-partials-modules-form-textarea) inside [form-field](#flf-form-layout-field)








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

### prmfe (partial modules form error)
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
### prmfir (partial modules form input radio)
```hbs
{{> modules/form field_type='input-radio' name='name' id='id' field_label='label' }}
```
### prmfic (partial modules form input checkbox)
```hbs
{{> modules/form field_type='input-checkbox' name='name' id='id' field_label='label'}}
```
### prmfif (partial modules form input file)
```hbs
{{> modules/form field_type='input-file'
  field_label='Profile Pic'
  name='profile_pic'
  input_id='profile_img'
  button_label='Choose Profile Pic'
}}
```
### prmffi (partial modules form field input)
```hbs
{{> modules/form field_type='form-field-input'
  type='text'
  name='first_name'
  mandatory='yes'
  field_label='First Name'
  placeholder='eg. Jhon Doe'
}}
```
### prmffa (partial modules form field addon )
```hbs
{{> modules/form field_type='form-field-addon'
  type='text'
  placement='start'
  addon_text='@'
  field_label='Tag your friend'
}}
```
### prmffd (partial modules form field datepicker)
```hbs
{{> modules/form field_type='form-field-datepicker'
  name='dob'
  mandatory='yes'
  field_label='Date of Birth'
}}
```
### prmfftp (partial modules form field timepicker)
```hbs
{{> modules/form field_type='form-field-timepicker'
  name='name'
  mandatory='yes'
  field_label='label'
}}
```
### prmfff (partial modules form field file)
```hbs
{{> modules/form field_type='form-field-file'
  name='avatar'
  mandatory='yes'
  field_label='Avatar'
  input_id='avatar'
  button_label='Upload Avatar'
}}
```
### prmffs (partial modules form field select)
```hbs
{{> modules/form field_type='form-field-select'
  typeOf='array|obj'
  name='month'
  select_values=monthArrary
  mandatory='yes'
  field_label='Select Month'
  placeholder='Month'
  opt_label='label'
  opt_value='url'
}}
```
> `opt_label` and `opt_value` is reserved for `typeOf='obj'` 

### prmfft (partial modules form field textarea)
```hbs
{{> modules/form field_type='form-field-textarea'
  name='comments'
  mandatory='yes'
  field_label='Comments'
  placeholder='Enter your message here'
}}
```



