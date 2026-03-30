# HTML Notes

> **HTML + CSS + JavaScript**  
> by 김기수 (Gilbut)

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
- Content **NOT** exists:
  - empty tag: `<br>`

### 4. Comment
  - Form: `<!-- Comment Content -->`

<br>

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

<br>

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

<br>

## Grouping
### 1. div tag
- Grouping block elements and inline elements together
- Form: `<div>...</div>`
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
- Form: `<span>...</span>`
- Example: `<p>The <span>highlight</span> scene of this movie is right here.</p>`
  - No change without applying CSS
 
<br>

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

<br>

## Inserts Links and Images
### 1. a tag
- Creates internal or external links in HTML
- Form: `<a href="Target URL or path" target="Link target behavior" title="Link description">...</a>`
- href: Specifies the target URL or path, required attribute
  - When the target URL is not specified: Sets the `href` attribute to `#`
  - Form: `<a href="#">Link</a>`
- target, title: optional attributes
  - target: Specifies how the link’s target is opened when creating a link
    - Attribute Value: _blank, _parent, _self, _top
      - Default: _self
      - Most Use: _blank
  - title: Text that describes the link
           (Provides additional information about the link)
    
Example:
```html
<a href="https://google.com" target="_blank">Go to Google</a>
```
<a href="https://google.com" target="_blank">Go to Google</a>

### 2. img tag
- Inserts an image object
- Form: `<img src="image path" alt="image description">`
- src (source): Specify the path of the image to be inserted
  - Can be a relative or absolute path

| Symbol | Description |
|:------:|:-----------:|
| ./ | Current Folder |
| ../ | Parent Folder |

- alt: Text that describes the inserted image object
- src, alt: Required attributes

### 3. Image Link
- `<img>` tag is placed inside an `<a>` tag: Clicking the image will navigate to the specified link
- Form:
```html
<a href="Target URL of path">
  <img src="Image path" alt="Alternative text">
</a>
```

<br>

## Text Emphasis
### 1. strong tag
- Indicates strong importance of the text
- Form: `<strong>Text with important meaning</strong>`

Example:
```html
<p>This facility is <strong>restricted to authorized personnel only</strong></p>
```
Example Output:  
<p>This facility is <strong>restricted to authorized personnel only</strong></p>

### 2. em tag
- Indicates emphasis in the text (changes the tone)
- Form: `<em>Text to be emphasized</em>`

Example:
```html
<p>It's dangerous from here, so <em>do not proceed</em> under any circumstances</p>
```
Example Output:
<p>It's dangerous from here, so <em>do not proceed</em> under any circumstances</p>  

<br>

## Creates a Form
- A form in HTML used to interact with the user, collect information, and send it to the server
- Includes various interactive elements such as fields for entering username and password, button elements, etc.

### 1. form tag
- Represents a form
- All form elements must be written inside the `<form>` tag
- Form: `<form action="Server URL" method="get or post">...</form>`
- Uses together with the action and method attributes
- action: URL of the server to which values entered through the form elements will be sent
  - Default: Current page URL
  - NOT send anywhere and stay on the current page: `#`
- method: The method used to send the entered values to the server (case-insensitive)
  - Default: get
  - Information that requires security: post
  
### 2. input tag
- Creates and input element, such as ID and password
- Attributes: type, name, value
  - type: required attribute
  - name, value: optional attributes
- Form: `<input type="type" name="name" value="default value">`
- type: Determines the type of interactive element based on the entered value
  
| Attribute value | Description |
|:---------------|:-----------|
| text | Single-line text input |
| password | Password input |
| tel | Enter a phone number format |
| number | Allows numeric input (with validation) |
| url | Enter a URL format |
| search | Enter search text |
| email | Enter email format |
| checkbox | Checkbox |
| radio | Radio button |
| file | File upload |
| button | Button element |
| image | Image as a button (like <img>; use src attribute, no alt) |
| hidden | Hidden input (not visible to the user) |
| date | Select a date (year, month, day)
| datetime-local | Select a date and time according to user timezone (year, month, day, hour, minute) |
| month | Select year and month |
| week | Select year and week |
| time | Select a time |
| range | Slider to select a numeric range |
| color | Select a color |
| submit | Button to submit a form |
| reset | Button to reset values entered in a form |

- name: Name of the input element
  - When the input element is sent to the server via a `<form>` tag, the value of the name attribute is used as its name
  - The server identifies the input element using this name
- value: Initial value of the input element
  - Input elements usually receive values manually from the user
  - This is used when an initial value needs to be set in certain situations
  
### 3. label tag
- Used to label interactive elements within a `<form>` tag
- Allows selecting the element by clicking the label
- Recommends for improving web accessibility
- Depending on how it is used, it can be classified into implicit and explicit methods
  - Implicit method: Include the interactive element inside the `<label>` tag
Eample:
```html
<label>
  ID
  <input type="text">
</label>
```
  - Explicit method: Set the for attribute of the `<label>` tag and the id attribute of the interactive element to the same value
Example:
```html
<label for="userpw">Password</label> <!-- for in this line and id in the below line have to have the same value -->
<input type="password" id="userpw">
```
  - Exceptionally, the implicit and explicit methods can be used together
Example:
```html
<label for="username">
  Name
  <input type="text" id="username">
</label>
```

### 4. fieldset and legend tag
- **fieldset**: Groups elements with a box-shaped border
- **legend**: Assigns a name to a group of elements
- Form:
```html
<form action="#">
  <fieldset>
    <legend>Group Name</legend>
    <!-- Omit interactive elements -->
  </fieldset>
</form>
```

### 5. textarea tag
- Creates a multi-line input element
- Defines the initial value within the content area (between the opening and closing tags)
- Form: `<textarea id="name" name="name">Initial Value</textarea>`
  - id, name: Optional attributes, but recommended
    - id should match the for attribute of label (for accessibility)
    
### 6. select, option, optgroup tag
- **select**: Creates a combo box
- **option**: Adds items to the combo box
- **optgroup**: Groups items together
- Form:
```html
<select>
  <optgroup label="Group Name">
    <option value="Value to be sent to the server">Value to be displayed in the web browser</option>
  </optgroup>
</select>
```
- option: The value to be sent to the server can be specified using the value attribute
  - value: If omitted, the text content is sent as the value
- optgroup: Specifies the group name using the label attribute
- Additional attributes: size, multiple, selected
  - size: Specifies the number of visible items in the combo box
    - Attribute value: number
    - Default value: 1 (when omitted)
    - Form: `<select name="name" id="name" size="3">`
  - multiple: Allows multiple items to be selected simultaneously
    - Window: Press Ctrl
    - Mac: Press cmd
    - Form: `<select name="name" id="name" multiple>`
  - selected: Default selected item can be changed
    - Default: The first `<option>` tag
    - Form: `<option value="name" selected>...</option>`
   
### 7. button tag
- Creation methods:
  - Sets the type attribute of an `<input>` tag to button
  - Creates separately using the `<button>` tag
    - Has a type attributes: submit, reset, button
      - submit: Purpose of submitting a form to the server
      - reset: Purpose of resetting the values entered in interactive elements
      - button: Simple button
    - Form: `<button type="type">Button Content</button>`
    
### 8. Additional Attributes in form-related Tags
- **disabled**: Disable interactive elements
  - User cannot interact with the element and its value is not submitted
    - Skipped when submitting the form
  - Can be used in: input, textarea, select, button tags
  - Input elements: Text cannot be entered
  - List boxes: Items cannot be selected
  - Button elements: Button cannot be clicked
  - Form: `<tag disabled>`
    - Example: `<input type="text" disabled>`
- **readonly**: Makes interactive elements read-only
  - User cannot edit the value, but it is still submitted with the form
  - Content can be selected or copied by dragging
  - Can be used in: textarea, input
    - Available type attribute values for the `<input>` tag:
      - text, search, url, tel, email, password, date, month, week, time, datetiem-local, number
  - Cannot edit + submitted
  - Form: `<tag readonly>`
    - Example: `<input type="password" readonly>`
- **maxlength**: Limits the number of characters that can be entered
  - Attribute Value: number
  - Can be used in: textarea, input
    - Available type attribute values for the `<input>` tag:
      - text, search, url, tel, email, password, date, month, week, time, datetiem-local, number
  - Form: `<tag maxlength="number">`
    - Example: `<input type="url" maxlength="4">`
- **checked**: Displays the element as selected
  - Can be used in: input
    - Available type attribute values for the `<input>` tag:
      - checkbox, radio (since a selectable element is required)
  - Form: `<tag checked>`
    - Example: `<input type="checkbox" id="name" name="name" value="name" checked>`
- **placeholder**: Provides a hint about what value should be entered in the input element
  - Form: `<input placeholder="Hint about Input Value">
    - Example: `<input type="tel" placeholder="Please enter the phone number">`

<br>

## Creates Table
- **Table**: Data arranged in a two-dimensional grid
  - Consists of **rows**, **columns**, and **cells** where rows and columns intersect

### 1. table tag
- Creates a table
- All table-related tags must be used inside the `<table>` tag
- Form: `<table>...</table>`

### 2. caption tag
- Specifies the table caption
- Optional, but **MUST** be written first inside the `<table>` tag when use
- Form:
```html
<table>
  <caption>Table Caption</caption>
</table>
```

### 3. tr tag
- Creates **a** row in a table
- Uses multiple times to create multiple rows
- Form:
```html
<table>
  <tr>...</tr>
</table>
```

### 4. th, td tags
- th(table header): Creates a column that represents a header in a table
- td(table data): Creates a column that represents regular data in a table
- Form:
```html
<table>
  <tr>
    <th>Header</th>
    <td>Data</td>
  </tr>
</table>
```

### 5. rowspan and colspan attributes
- **rowspan**: Merges rows
- **colspan**: Merges columns
- Attribute value: Number of cells to be merged
  - Leave the next row or column empty for the number of merged cells
- Form: `<td rowspan="number">...</td>`
        `<td colspan="number">...</td>`
        
### 6. thead, tfoot, tbody tags
- **thead**: Groups rows that correspond to the *header* section
- **tfoot**: Groups rows that correspond to the *footer* section
- **tbody**: Groups rows that correspond to the *body* section
- Optional, but the **order MUST be thead, tfoot, tbody** when use
- thead, tfoot: Can be used **ONLY once**
  - Rows grouped with `<thead>` must use `<th>` tags to create columns
- Form:
```html
<table>
  <thead>
    <th>...</th>
  </thead>
  <tfoot>
    <td>...</td>
  </tfoot>
  <tbody>
    <td>...</td>
  </tbody>
</table>
```

### 7. col and colgroup tags
- **col**: Groups a single column
- **colgroup**: Groups two or more columns
  - Uses with the span attribute
- Primarily use to group an entire column to apply a uniform style
- **MUST** uses after the `<caption>` tag if caption tag was used.
  - The number of `<col>` or `<colgroup>` tags **MUST** match the number of columns used
- **MUST** uses befroe the `<tr>` tag
- Form:
```html
<col>
<colgroup span="Number of columns to be grouped">
```

### 8. scope attribute
- Only for improving web accessibility
- Specifies the scope of a header cell
- Can **ONLY** be used with `<th>` tag
- Attribute Values: col, row, colspan, rowspan
- Form: `<th scope="row">...</th>` `<th scope="col">...</th>`

<br>

## Multimedia Settings
### 1. audio tag
- Form: `<audio src="Audio File Path" controls></audio>`
- src: Required attribute
- controls: Displays the audio control panel

Audio file formats supported by each web browser
| Web Browser | MP3 | WAV | OGG |
|:------------|:---:|:---:|:---:|
| Internet Explorer (IE) | O | X | X |
| Edge | O | O | O |
| Chrome | O | O | O |
| Firefox | O | O | O |
| Safari | O | O | X |
| Opera | O | O | O |

Media types for each audio file format
| File Format | Media Types |
|:------------|:------------|
| MP3 | audio/mpeg |
| WAV | audio/wav |
| OGG | audio/ogg |

### 2. video tag
- Form: `<video src="Video File Path" controls></video>`
- src: Required attribute
- controls: Displays a control panel that the user can operate

Video file formats supported by each web browser
| Web Browser | MP4 | WebM | Ogg |
|:------------|:---:|:---:|:---:|
| Internet Explorer (IE) | O | X | X |
| Edge | O | O | O |
| Chrome | O | O | O |
| Firefox | O | O | O |
| Safari | O | O | X |
| Opera | O | O | O |

Media types for each video file format
| File Format | Media Types |
|:------------|:------------|
| MP4 | video/mp4 |
| WebM | video/webm |
| OGG | video/ogg |

### 3. source tag
- Specifies the resource (file) path and media type in <audio> and <video> tags
- Optional, but recommended for web accessibility by registering multimedia in various formats
- Form:
```html
<audio controls>
  <source src="File Path" type="Media Type">
</audio>
<video controls>
  <source src="File Path" type="Media Type">
</video>
```

## Semantic tags for designing the structure of a web page
- Semantic tag: The purpose or role of the tag is clear from its name alone
### 1. header tag
- Defines the header section in a web page
- Form:
```html
<header>
  Header components
</header>
```

### 2. nav tag
- Defines the navigation area that links to other sections within the page or to external pages
- Form: `<nav>...</nav>`

### 3. section tag
- Defines a **logically related content area** in a web page
- Usually contains one of the `<h1>`–`<h6>` heading tags
- Form: `<section>...</section>`

### 4. article tag
- Defines an **independently usable content area** in a web page
- Form: `<article>...</article>`

### 5. aside tag
- Uses for content that is not considered the main content or independent content of the page and cannot be marked as an `<article>` or `<section>`
- Represents content indirectly related to the main content (e.g., sidebar, ads, related links)
- Form: `<aside>...</aside>`

### 6. footer tag
- Defines the footer area of a web page
- Usually at the bottom of the page
- Contains elements such as copyright information, contact details, or a site map
- Form: `<footer>...</footer>`

### 7. main tag
- Specifies the main content of a web page
- Should not include elements that appear repeatedly across pages
- Should not be placed inside `<article>`, `<aside>`, `<footer>`, `<header>`, or `<nav>` elements
- Form: `<main>...</main>`

<br>

## Global attributes that can be used regardless of the tag type
- Attributes that can be used commonly across all tags, regardless of tag type

Frequently used global attributes
| Attributes | Value | Description |
|:-----------|:------|:------------|
| class | value | Assigns a class value to an element<br>Class value: Can be used as a class selector in CSS |
| id | value | Assigns an ID value to an element<br>ID value: Can be used as an ID selector in CSS |
| style | style | Applies inline styles to an element |
| title | text | Specifies additional information for an element<br>The additional information is displayed as a tooltip when the mouse hovers over the element<br>Tooltip: A balloon-shaped graphic that shows extra description |
| lang | language code | Specify the language information of the text used in an element |
| hidden | hidden | Hide an element from the screen |
| data-* | value | Allows the user to create custom attributes |

- **class** attribute: Assigns one or more class names to an element
  - Can be used as a class selector in CSS
  - The same class name can be shared by multiple elements
  - Form: `<p class="red-color">...</p>`
- **id** attribute: Assigns an ID to an element
  - Can be used as an ID selector in CSS
  - **MUST** be unique
  - Form: `<h1 id="title">...</h1>`
- **style** attribute: Used to apply inline CSS styles to an element
- **title** attribute: Used to provide additional information about an element
  - Displays as a tooltip when the mouse hovers over the element
  - Form: `<p><span title="Additional Information">...</span></p>`
- **lang** attribute: Specifies the language of the content in an element
  - Usually set in the lang attribute of the `<html>` tag
  - Form: `<html lang="ko">` `<p lang="de">Guten Tag</p>`
- **data-\*** attribute: Creates custom attributes for the user
  - Example: `<p data-name="spiderMan" data-hero="true">...</p>`
