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
