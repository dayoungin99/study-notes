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


## Writing text
1. hn tag: Used to represent text that indicates a title or topic
- Form: \<hn>Title</hn>
- Six heading tags: \<h1> to \<h6>
- \<h1> is the most important, and \<h6> is the least important
- Text in \<h1> is the largest and boldest, and the size and weight gradually decrease from \<h2> to \<h6>
- Search engines: Crawling headings from <h1> in order, so if \<h4> is skipped, \<h5> and \<h6> are not crawled
2. p tag: Used to write paragraphs in the main content
- Form: \<p>Content</p>
3. br tag: Used to insert a line break within a paragraph
- Form: \<br>
4. blockquote tag: Used to write block-level text quoted from a source
- Form: \<blockquote cite="Source URL">Block-level text</blockquote>
- For verified quotations, the source URL or reference should be specified using the cite attribute
5. q tag: Used to write short, inline quotations within a paragraph
- Form: \<q cite="Source URL">Short quotations</q>
- content inside the <q> tag is enclosed in quotation marks ("")
6. ins and del tags: Used to indicate newly added or deleted text
- Form: \<ins>Added text</ins>
        \<del>Deleted text</del>
- Content inside the <ins> tag is <u>underlined</u>
- Content inside the <del> tag has a ~~strikethrough~~
7. sub and sup tags: Used to write subscript and superscript text
- Form: \<sub>Subscript text</sub>
      \<sup>Superscript text</sup>
- sub example: H<sub>2</sub>O
- sup example: 4<sup>2</sup> = 16
