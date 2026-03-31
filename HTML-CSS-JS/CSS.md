# CSS Notes

> **HTML + CSS + JavaScript**  
> by 김기수 (Gilbut)

## Basic CSS
### 1. Syntax
- **Selector**: Targets the HTML tag (element) to which the CSS styles will be applied
- **Declaration Block**: Writes the styles to be applied to the tag selected by the selector
  - Placed inside curly braces({})
  - Must be written as a property-value pair
  - Adding a semicolon(;) after a value: Writes multiple styles consecutively
  
  Example:
  ```css
  h1{
    font-size:24px;
    color:red;
  }
  ```
<br>

## Applying CSS
### 1. Using Internal Style Sheets
- Writes CSS code inside an HTML file
- Writes CSS code as the content of the HTML <style> tag
- Usually used inside the `<head>` tag
- Form:
  ```css
  <style>
    /* CSS Code */
  </style>
  ```
  
Example:
```css
<head>
  <title>Internal Style Sheets</title>
  <style>
    h1{
      color:blue;
    }
  </style>
<head>
<body>
  <h1>Internal Style Sheets></h1>
</body>
```

### 2. Using External Style Sheets
- Creates a separate file to write CSS code and links it to the HTML document
- Extension of the separate file: .css
  - Use the <link> tag to connect it in the HTML document
- Most common
- Form: `<link rel="stylesheet" href="css file path">`

### 3. Using Inline Style
- Writes CSS code in the style attribute that can be used in HTML tags
- Writes CSS code directly in the tag
  - Selector part in the basic CSS syntax is not required
- Form: `<tag style="CSS code">...</tag>`

<br>

## Using Basic Selectors
### 1. Universal Selector
- Selects all elements in HTML at once as a selector
- Using the * symbol
- Form: `*{/* CSS Code */}`

### 2. Tag Selector
- Specifies the selector using the HTML tag name
- Selects all elements that match the tag name specified in the selector at once
- Form: `tagname{/* CSS Code */}`

### 3. ID Selector
- Specifies the selector using the value of the id attribute in an HTML tag
- Prefix the value with the **#** symbol to distinguish it
- **MUST** be a unique value within a single HTML document
- Form: `#id-attribute-value{/* CSS Code */}`

### 4. Class Selector
- Specifies the selector using the value of the class attribute in an HTML tag
- Adds a dot (.) prefix to the property value
- Most common
- class attribute:
  - Can have reusable values
  - Can be applied in multiple places if a class is well defined
- Form: `.class-attribute-value{/* CSS Code */}`

### 5. Basic Attribute Selector
- Defines a selector using an HTML element’s attribute and its value
- Form: `[attribute]{/* CSS Code */}`
  - Selects all elements with the same attribute, regardless of its value and element type
- Specifies both the attribute and its value to apply styles only to elements that exactly match them
- Form: `[attribute=value]{/* CSS Code */}`
- Can be used together with other selectors: Tag, ID, Class Selectors
  - Form: `tag/id/class-selector[attribute-selector]{}`
 
### 6. String Attribute Selector
- Selects elements whose attribute value exactly matches a specific string
- Basic principle: similar to the basic attribute selector, but uses a different matching method

Format of a string attribute selector

| Format | Description |
|:-------|:------------|
| \[attribute~=string] | Selects elements whose attribute value contains the string (word-based) |
| \[attribute|=string] | Selects elements whose attribute value is exactly the string <br>or starts with the string followed by a hyphen |
| \[attribute^=string] | Selects elements whose attribute value starts with the string
| \[attribute$=string] | Selects elements whose attribute value ends with the string
| \[attribute*=string] | Selects elements whose attribute value contains the string (based on the entire value)

<br>

## Using a Combinator Selector
- Combinator selector: a selector that enriches the meaning when used together with a basic selector

### 1. Group Selector
