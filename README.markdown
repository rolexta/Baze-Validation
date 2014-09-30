# Baze Validation


> Validate your form with ease using Baze Validation

Baze Validation will validate:
* Empty fields
* Email format
* More to come

## Install

Install Baze Validation by running
```
bower install baze-validation --save
```
or download from the [project release](https://github.com/ImBobby/Baze-Validation/releases). 

Then include jQuery and `baze.validation.js` via script tag.

```HTML
<script src="jquery.js"></script>
<script src="baze.validation.js"></script>
```

## How to use

Init the plugin by doing this

```Javascript
BazeValidate.run();
```

### API

Baze Validation expose these APIs

| API   | Description  |
|---|---|
| `run()`  | Trigger Baze Validation  |
| `setErrorClass( string )`  | set class name for invalid fields. default: **form-input--error**   |
| `setSuccessClass( string )`  | set class name for valid fields. default: **form-input--success**   |
| `setMsgClass( string )`  | set class name for form message. default: **form-msg-error**   |


## How it works

Baze Validation will validate any `<form>` element that has `data-baze-validate` attribute and `required` attribute on its children. 
```HTML
<form data-baze-validate>
    <label for="username">Username</label>
    <input id="username" type="text" required>
    
    ...
</form>
```

**Baze Validation will not validate a form if `data-baze-validate` attribute is not specified and has no `required` attribute on its children.**

Baze Validation will listen on form submit event. When a form submit event is triggered, it will:


1. Check for empty fields.
2. If field is invalid, class `form-input--error` will be added. A message will be placed after the field with class `form-msg-error`.
3. If field is valid, class `form-input--success` will be added.

**Baze validation has no default styling so it is up to you how you want to style it.**