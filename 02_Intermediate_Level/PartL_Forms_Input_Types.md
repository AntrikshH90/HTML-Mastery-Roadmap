# 🅻 PART L: FORMS & ALL INPUT TYPES

## 📖 Theory (from PDF)

> HTML form is used to **collect user input** in the webpage and can then be sent to the server for processing. To add the form we use the `<form>` element.

## Form Attributes (from PDF)

| Attribute | Description (from PDF) |
|-----------|----------------------|
| `name` | Defines name of the form, it should be unique. Useful for accessing form in JavaScript |
| `action` | Specifies URL where the form data will be sent when submitted. Path to backend script which processes the data |
| `method` | Used to set HTTP method: **GET** (sends data as URL parameter, visible) or **POST** (sends in request body, more secure) |
| `enctype` | Defines how browser should encode data: **application/x-www-form-urlencoded** (default), **multipart/form-data** (for file uploads), **text/plain** (debugging) |

## Form Field Types (from PDF)

The PDF lists these field types:
- Text Fields
- Buttons
- Checkbox
- Radiobox
- Select options control
- File select
- Hidden inputs
- Labels

## All Input Types (from PDF + Extended)

### Text Inputs

```html
<!-- Text (from PDF): A single line text field (Default) -->
<input type="text" name="username">

<!-- Password (from PDF): Characters are masked/hidden -->
<input type="password" name="password">

<!-- Email (from PDF): Includes basic validation -->
<input type="email" name="email">

<!-- Tel (from PDF): For telephone numbers -->
<input type="tel" name="phone">

<!-- Search (from PDF): Designed for search inputs -->
<input type="search" name="search">

<!-- URL -->
<input type="url" name="website" placeholder="https://example.com">
```

### Number & Range Inputs

```html
<!-- Number (from PDF): Accepts integers with optional min, max, step -->
<input type="number" name="age" min="1" max="100">

<!-- Range (from PDF): A slider to select value between specified range -->
<input type="range" name="volume" min="0" max="100" step="10">
```

### Date/Time Inputs (HTML5 — from PDF)

```html
<!-- Date (from PDF): Select date from drop-down calendar -->
<input type="date" name="date">

<!-- DateTime (from PDF): Select date and time at same time -->
<input type="datetime-local" name="DateTime">

<!-- Time (from PDF): Select time -->
<input type="time" name="time">

<!-- Month -->
<input type="month" name="birth-month">

<!-- Week -->
<input type="week" name="project-week">
```

### Selection Inputs

```html
<!-- Radio (from PDF): Select one option from group -->
<!-- For grouping, use same name for all radio buttons -->
<input type="radio" name="gender" id="male" value="male">
<label for="male">Male</label>
<input type="radio" name="gender" id="female" value="female">
<label for="female">Female</label>

<!-- Checkbox (from PDF): Select one or more options from group -->
<!-- For grouping, use same name for all checkboxes -->
<input type="checkbox" name="subscribe" id="sub" value="yes">
<label for="sub">Subscribe to Newsletter</label>
```

### Checkbox Attributes (from PDF)

| Attribute | Description (from PDF) |
|-----------|----------------------|
| `type` | Set to `checkbox` |
| `name` | Name of the checkbox |
| `id` | ID of the checkbox |
| `onChange` | JavaScript function when user checks/unchecks |
| `value` | Value of checkbox (e.g., food name) |
| `checked` | If added, checkbox is selected by default |

### Radio Button Attributes (from PDF)

| Attribute | Description (from PDF) |
|-----------|----------------------|
| `type` | Set to `radio` |
| `name` | Name of the radio button (same name = same group) |
| `id` | ID of the radio button |
| `onChange` | JavaScript function when checked/unchecked |
| `value` | Value of the radio button |
| `checked` | If added, radio button is selected by default |

### Other Input Types

```html
<!-- Color (from PDF): Color picker -->
<input type="color" name="favcolor">

<!-- File (from PDF): File upload -->
<input type="file" name="myfile">
<input type="file" name="avatar" accept="image/*" multiple>

<!-- Hidden (from PDF): Stores data without displaying to user -->
<input type="hidden" name="userID" value="12345">

<!-- Submit (from PDF): Button to submit form data -->
<input type="submit" value="Login">

<!-- Reset (from PDF): Resets all fields to initial value -->
<input type="reset" value="Reset">

<!-- Image (from PDF): Graphical version of submit button -->
<input type="image" src="icon.jpg" alt="Submit">
```

## File Input Important Note (from PDF)

> While adding file input control, **never forget** to set `enctype="multipart/form-data"` attribute in the form element.

## Labels (from PDF)

> We can use `<label>` to set a label for the input field. When users click on the label, the form field **automatically gets selected**. For this feature, set the `for` attribute in the label and it should match with the input field `id`.

```html
<!-- Explicit label (recommended — from PDF) -->
<label for="name">Name:</label>
<input type="text" name="name" id="name">

<!-- Implicit label (wrapping) -->
<label>
    Email:
    <input type="email" name="email">
</label>
```

> ⚠️ **Always use labels!** They improve accessibility and increase click target area.

## Textarea (from PDF)

> Creates multi-line text input area. Useful for larger blocks of text like user address and description.

| Attribute | Description (from PDF) |
|-----------|----------------------|
| `name` | Name of the field |
| `id` | ID of the field |
| `rows` | Number of rows for text area |
| `cols` | Number of columns for text area |

```html
<label for="address">Address:</label>
<textarea name="address" id="address" cols="30" rows="10"></textarea>
```

## Select Dropdown (from PDF)

> If you have a long list of options and you want to allow select only one option, use **select input** type instead of radio buttons.

```html
<label for="country">Country:</label>
<select name="country" id="country">
    <option value="" disabled selected>-- Select --</option>
    <option value="india">India</option>
    <option value="usa">USA</option>
</select>
```

## Optgroup (from PDF)

> Used to **group options** inside a select dropdown list for easier navigation.

```html
<select name="tech">
    <optgroup label="Front-End">
        <option value="-1">Select tech</option>
        <option value="html">HTML</option>
        <option value="css">CSS</option>
    </optgroup>
    <optgroup label="Back-end">
        <option value="java">Java</option>
        <option value="php">PHP</option>
    </optgroup>
</select>
```

## Button (from PDF)

> Creates clickable buttons. Used to submit form data and also to perform actions with JavaScript.

| Attribute | Description (from PDF) |
|-----------|----------------------|
| `type` | Type: `submit`, `reset`, `button` |
| `name` | Name of the button |
| `id` | ID of the button |
| `onClick` | JavaScript function when clicked |

```html
<button type="submit">Submit</button>
<button type="reset">Reset</button>
<button type="button" onclick="alert('Hi!')">Click Me</button>
```

## Fieldset & Legend (from PDF)

> Fieldset **groups related fields** in the form. Legend provides a **caption** to the group.

```html
<fieldset>
    <legend>Personal Information</legend>
    <label for="fname">First Name:</label>
    <input type="text" id="fname" name="fname">
</fieldset>
```

## Datalist (from PDF)

> Provides list of **predefined options** to input field.

```html
<input list="mylist" name="city">
<datalist id="mylist">
    <option value="Pune"></option>
    <option value="Mumbai"></option>
    <option value="Delhi"></option>
</datalist>
```

## Hidden Input Explained (from PDF)

> If you want to add/set a value in the form that can be used later or sent to the server **without showing it to the user**, hidden fields are used. For example, you need a user ID for front-end operations but don't want to show it.

```html
<input type="hidden" name="user-id" value="12345">
```

## Additional Input Attributes

| Attribute | Description |
|-----------|-------------|
| `required` | Must be filled before submit |
| `readonly` | Can't be edited (still submitted) |
| `disabled` | Can't be edited (NOT submitted) |
| `placeholder` | Hint text inside input (from PDF) |
| `value` | Initial value of field (from PDF) |
| `autofocus` | Auto-focus on page load |
| `autocomplete` | Browser auto-fill |
| `pattern` | Regex validation |
| `min` / `max` | Minimum/maximum value |
| `minlength` / `maxlength` | Character limits |
| `step` | Number increment value |
| `multiple` | Allow multiple values (email, file) |
| `accept` | File types accepted |
| `inputmode` | Virtual keyboard hint (`numeric`, `tel`, `email`, `url`) |
| `enterkeyhint` | Label for Enter key (`search`, `send`, `go`, `next`, `done`) |

## Complete Form Example (from PDF Page 18)

```html
<!DOCTYPE html>
<html>
<head>
    <title>HTML Forms</title>
</head>
<body>
    <section>
        <form name="user_form" method="post" action="/my_action">
            <label for="name">Name:</label> 
            <input type="text" name="name" id="name" value=""><br>
            
            <label for="password">Password:</label> 
            <input type="password" name="password" id="password" value=""><br>
            
            <label for="address">Address:</label> 
            <textarea name="address" id="address" cols="30" rows="10"></textarea><br>
            
            <label for="checkbox">Checkbox:</label> 
            <input type="checkbox" name="checkbox" id="checkbox" value="checkbox_1"><br>
            
            <label for="checkbox_2">Checkbox 2:</label> 
            <input type="checkbox" name="checkbox" id="checkbox_2" value="checkbox_2"><br>
            
            <label for="radio">Radio:</label> 
            <input type="radio" name="radio" id="radio" value="radio"><br>
            
            <label for="radio_2">Radio:</label> 
            <input type="radio" name="radio" id="radio_2" value="radio_2"><br>
            
            <label for="select">Select:</label> 
            <select name="select" id="select">
                <option value="option_1">Option 1</option>
                <option value="option_2">Option 2</option>
                <option value="option_3">Option 3</option>
            </select><br>
            
            <label for="file">File:</label> 
            <input type="file" name="file" id="file" value=""><br>
            
            <label for="hidden">Hidden:</label> 
            <input type="hidden" name="hidden" id="hidden" value="12"><br>
            
            <input type="submit" value="Submit">
        </form>
    </section>
</body>
</html>
```

## HTML5 New Input Types Example (from PDF Page 19)

```html
<form name="user_form" method="post" action="/my_action">
    <label for="date">Date</label> 
    <input type="date" name="date" id="date" value=""><br>
    
    <label for="time">Time</label> 
    <input type="time" name="time" id="time" value=""><br>
    
    <label for="DateTime">DateTime</label> 
    <input type="datetime-local" name="DateTime" id="DateTime" value=""><br>
    
    <label for="email">Email</label> 
    <input type="email" name="email" id="email" value=""><br>
    
    <label for="url">URL</label> 
    <input type="url" name="url" id="url" value=""><br>
    
    <label for="number">Number</label> 
    <input type="number" name="number" id="number" value=""><br>
    
    <label for="range">Range</label> 
    <input type="range" name="range" id="range" value=""><br>
    
    <label for="tel">Telephone</label> 
    <input type="tel" name="tel" id="tel" value=""><br>
    
    <label for="color">Color</label> 
    <input type="color" name="color" id="color" value=""><br>
</form>
```

## Output & Progress Elements

```html
<!-- Output element -->
<form oninput="result.value = parseInt(a.value) + parseInt(b.value)">
    <input type="number" id="a" name="a" value="10"> +
    <input type="number" id="b" name="b" value="20"> =
    <output name="result" for="a b">30</output>
</form>

<!-- Progress bar -->
<label for="upload">Upload progress:</label>
<progress id="upload" value="70" max="100">70%</progress>

<!-- Meter (gauge) -->
<label for="disk">Disk usage:</label>
<meter id="disk" value="0.7" min="0" max="1" 
       low="0.3" high="0.7" optimum="0.2">70%</meter>
```

---

