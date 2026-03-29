# Study with HTML + CSS + JavaScript, <br>written by 김기수, Published from gilbut

## HTML Basic Components
### 1. Tag
  - Form: \<TagName>
### 2. Attributions
  - Form: \<TagName AttrName="AttrValue">
### 3. Symtax  
- Content exists:
  - ex) \<title>My First Web Page!</title>  
    - \<title>: Open tag  
    - My First Web Page!: Content  
    - \</title>: Close tag  
    - \<title> ... \</title>: Element  
- Content NOT exists:
  - empty tag: \<br>
### 4. Comment
  - Form: \<!-- Comment Content -->

  
## HTML Basic Structure
```html
<!-- Use ! for writing the basic structure automatically -->
<!DOCTYPE html> <!-- DTD(Document Type Definition): Defines the document type and tells the browser which HTML standard to use -->
<html lang="en"> <!-- html: The beginning and end of an HTML document -->
<head> <!--head: Defines the metadata of the HTML document
                 (Metadata: Information about the HTML document, NOT directly displayed in the web browser;
                            commonly used tags include <meta>, <title>, <link>, <style>, <script>, etc) -->
    <meta charset="UTF-8"> <!-- Defines the charset used in the HTML document -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- Used to make the page fit the device’s screen width;
                                                                                Viewport: Visible area of a web page to the user -->
    <title>My First Web Page!</title> <!-- title: Specifies the title of the HTML document, MUST be unique within each HTML document -->
</head>
<body> <!-- Writes content that is displayed in the web browser -->
    <p>My First Web Page</p>
</body>
</html>
```
