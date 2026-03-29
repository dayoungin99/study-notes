# Study with HTML + CSS + JavaScript, <br>written by 김기수, Published from gilbut

## HTML Basic Components
### 1. Tag
  - Form: `<TagName>`
### 2. Attributions
  - Form: `<TagName AttrName="AttrValue">`
### 3. Symtax  
- Content exists:
  - ex) `<title>My First Web Page!</title>`  
    - \<title>: Open tag  
    - My First Web Page!: Content  
    - \</title>: Close tag  
    - \<title> ... \</title>: Element  
- Content NOT exists:
  - empty tag: `<br>`
### 4. Comment
  - Form: `<!-- Comment Content -->`

  
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


## HTML Text Elements
### 1. hn tag
- Represents a title or topic
- Form: `<hn>Title</hn>`
- Six levels: \<h1> to \<h6>
- `<h1>` is the most important
- Size decreases from `<h1>` to `<h6>`
- Headings should follow a logical order for better SEO
### 2. p tag
-Writes paragraphs in the main content
- Form: `<p>Content</p>`
### 3. br tag
- Inserts a line break within a paragraph
- Form: `<br>`
### 4. blockquote tag
- Writes block-level text quoted from a source
- Form: `<blockquote cite="Source URL">Block-level text</blockquote>`
- For verified quotations, the source URL or reference should be specified using the cite attribute
### 5. q tag
- Writes short, inline quotations within a paragraph
- Form: `<q cite="Source URL">Short quotations</q>`
- content inside the `<q>` tag is enclosed in quotation marks ("")
### 6. ins and del tags
- Indicates newly added or deleted text
- Form: `<ins>Added text</ins>`
        `<del>Deleted text</del>`
- Content inside the `<ins>` tag is <u>underlined</u>
- Content inside the `<del>` tag has a ~~strikethrough~~
### 7. sub and sup tags
- Writes subscript and superscript text
- Form: `<sub>Subscript text</sub>`
        `<sup>Superscript text</sup>`
- sub example: H<sub>2</sub>O
- sup example: 4<sup>2</sup> = 16


## Grouping
### 1. div tag
- Grouping block elements and inline elements together
- Form: `<div> </div>`
```html
<!-- Code can be more complicated without section division -->
<body>
  <p>Movie Introduction</p>
  <p>This is a page introducing a movie.</p>
  <p>TV Show Introduction</p>
  <p>This is a page introducing a TV show.</p>
</body>

<!-- Grouping by sections -->
<body>
  <div class="movie">
    <p>Movie Introduction</p>
    <p>This is a page introducing a movie.</p>
  </div>
  <div class="tv">
    <p>TV Show Introduction</p>
    <p>This is a page introducing a tv show.</p>
  </div>
</body>
```
### 2. span tag
- Grouping inline elements
- Form: `<span> </span>`
- Example: `<p>The <span>highlight</span> scene of this movie is right here.</p>`
  - No change without applying CSS
 

## List
### 1. ul tag
- Creates an unordered list (bullet list)
- Form:
```html
<ul>
  <li>List Content 1</li>
  <li>List Content 2</li>
</ul>
```
Example output:
<ul>
  <li>List Content 1</li>
  <li>List Content 2</li>
</ul>

### 2. ol tag
- Creates an ordered list (numbered list)
- Form:
```html
<ol>
  <li>List Content 1</li>
  <li>List Content 2</li>
</ol>
```
Example output:
<ol>
  <li>List Content 1</li>
  <li>List Content 2</li>
</ol>

### 3. dl tag
- Creates a definition list (a list of terms and their descriptions)
- Use `<dt>` for terms and `<dd>` for descriptions (instead of `<li>`)
- Form:
```html
<dl>
  <dt>Term 1</dt>
  <dd>Description 1</dd>
  <dt>Term 2</dt>
  <dd>Description 2</dd>
</dl>
```
Example output:
<dl>
  <dt>Term 1</dt>
  <dd>Description 1</dd>
  <dt>Term 2</dt>
  <dd>Description 2</dd>
</dl>


## Inserts Links and Images
