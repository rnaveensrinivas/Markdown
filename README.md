# Table of Contents
* [Introduction](#introduction)
* [Basic Syntax](#basic-syntax)
  * [Headings](#headings)
  * [Paragraphs](#paragraphs)
  * [Line Breaks](#line-breaks)
  * [Emphasis](#emphasis)
    * [Bold](#bold)
    * [Italic](#italic)
    * [Bold and Italic](#bold-and-italic)
    * [Strikethrough](#strikethrough)
    * [Underline](#underline)
    * [Highlight](#highlight)
  * [Blockquotes](#blockquotes)
  * [Lists](#Lists)
  * [Inline Code](#Inline-code)
  * [Code Blocks](#code-blocks)
  * [Horizontal Rules](#horizontal-rules)
  * [Links](#links)
  * [Images](#images)
  * [Escaping Characters](#escaping-characters)
  * [Subscript Text](#subscript-text)
  * [Superscript Text](#superscript-text)
* [Extended Syntax](#extended-syntax)
  * [Tables](#tables)
  * [Syntax Highlighting for Fenced Code Blocks](#syntax-highlighting-for-fenced-code-blocks)
  * [Heading IDs](#heading-ids)
  * [Task Lists](#task-lists)
  * [Automatic URL Linking](#automatic-url-linking)
  * [Disabling Automatic URL Linking](#disabling-automatic-url-linking)
  * [Emoji](#emoji)
* [LaTeX Mathematical Notation](#latex-mathematical-notations)
  * [Inline Math](#inline-math)
  * [Block Math](#block-math-display-math)
  * [Superscripts and Subscripts](#superscripts-and-subscripts)
  * [Fractions](#fractions)
  * [Square Roots](#square-roots)
  * [Greek Letters](#greek-letters)
  * [Summation and Product Notation](#summation-and-product-notation)
  * [Limits](#limits)
  * [Integral Notation](#integral-notation)
  * [Matrices](#matrices)
  * [Aligning Equations](#aligning-equations)
  * [Exponents and Logarithms](#exponents-and-logarithms)
  * [Binomial Coefficient](#binomial-coefficient)
  * [Brackets and Parantheses](#brackets-and-parentheses)
  * [Derivatives and Differential Operators](#derivatives-and-differential-operators)
  * [Angle Notations](#angle-notations)
  * [Vectors and Matrices](#vectors-and-matrices)
  * [Absolute Value](#absolute-value)
  * [Complex Expressions](#complex-expressions)
* [**Cheat sheet**](#cheat-sheet)
---

# Introduction

Markdown is a lightweight, widely-used, and highly successful **markup language** created by John Gruber in 2004. It allows you to add formatting elements to plain text documents using simple syntax. For example, you can create headings with the `#` symbol.

### Key Features of Markdown:
- **Readable and Unobtrusive**: The syntax is designed to be as readable as plain text, even before rendering. This makes Markdown documents easy to read and work with, even in their raw form.
  
  > *The overriding design goal for Markdown's formatting syntax is to make it as readable as possible. The idea is that a Markdown-formatted document should be publishable as-is, as plain text, without looking like it's been marked up with tags or formatting instructions.*

- **Replaces WYSIWYG Editors**: Markdown has become a modern alternative to **WYSIWYG** (What You See Is What You Get) editors for creating formatted documents.
- **Simple Yet Powerful**: Markdown is easy to learn and powerful enough to create everything from basic documents to complex technical manuals.
- **Versatile Applications**: It is used across a wide range of domains, including:
  - Websites
  - Documentation
  - Notes
  - Books
  - Presentations
  - Emails

- **In-Demand Skill**: Fun fact: Proficiency in Markdown is often a requirement in job descriptions, especially for roles involving technical writing or documentation.

---

## How Does Markdown Work?

Markdown works through a simple conversion process: 

1. Write your content in a **Markdown file** with an extension like `.md` or `.markdown`.  
2. Pass the file into a **Markdown application**, which includes a **Markdown processor** (also called a "parser" or "implementation").
3. The processor converts Markdown syntax into **HTML**.

### Workflow Diagram
```plaintext
Markdown (.md) -> Markdown Application (contains Markdown Parser) -> HTML (.html)
```

This streamlined process makes Markdown both efficient and powerful, making it the go-to choice for creating structured and formatted content.

---

# Basic Syntax

Markdown's basic constructs were introduced by its creator, **John Gruber**, and remain at the core of its simplicity and effectiveness. 

> **Note**: You can seamlessly use HTML tags within Markdown files for additional customization.

---

## Headings

Headings in Markdown are created using the `#` symbol. The number of `#` symbols corresponds to the heading level, from 1 (largest) to 6 (smallest).

| Markdown               | HTML                           |
|-------------------------|--------------------------------|
| `# Heading level 1`    | `<h1>Heading level 1</h1>`    |
| `## Heading level 2`   | `<h2>Heading level 2</h2>`    |
| `### Heading level 3`  | `<h3>Heading level 3</h3>`    |
| `#### Heading level 4` | `<h4>Heading level 4</h4>`    |
| `##### Heading level 5`| `<h5>Heading level 5</h5>`    |
| `###### Heading level 6`| `<h6>Heading level 6</h6>`  |

### Alternate Syntax for Levels 1 and 2
For **Heading Level 1** and **Heading Level 2**, you can use `=` and `-` underlines as an alternative to `#`:

### Example
#### Markdown:
```markdown
Heading level 1
===============

Heading level 2
---------------
```

#### HTML Conversion: 
```HTML
<h1>Heading level 1</h1>

<h2>Heading level 2</h2>
```

#### Rendered Output:
Heading level 1  
===============  

Heading level 2  
---------------  

---

## Paragraphs

Paragraphs are created by separating blocks of text with a blank line. Each block becomes a paragraph in the rendered output.

### Example
#### Markdown: 
```markdown
I really like using Markdown.

I think I'll use it from now on.
```

#### HTML Conversion:
```html
<p>I really like using Markdown.</p>

<p>I think I'll use it from now on.</p>
```

#### Rendered Output:
I really like using Markdown.  

I think I'll use it from now on.

---

## Line Breaks

Line breaks in Markdown allow you to control where text starts on a new line within the same paragraph.

### How to Add Line Breaks
#### Use the HTML `<br>` tag
Add a `<br>` tag wherever you want to insert a line break.

```markdown
This is the first line.<br>
And this is the second line.
```

#### Use Double Spaces
Add **two spaces** (`  `) at the end of a line, followed by pressing **Enter**.

```markdown
This is the first line.  
And this is the second line.
```

### Example

#### Markdown:
```markdown
This is the first line.  
And this is the second line.
```

#### HTML Conversion:
```html
<p>This is the first line.<br />
And this is the second line.</p>
```

#### Rendered Output:
This is the first line.  
And this is the second line.

---

## Emphasis

Markdown provides simple ways to emphasize text using **bold**, *italic*, or a combination of both. You can also use **strikethrough** and **underline**, though the latter requires HTML.

---

### Bold
To create bold text, use **two asterisks (`**`)** or **two underscores (`__`)** before and after the text. 

| Markdown                  | HTML                              | Rendered Output         | 
|---------------------------|-----------------------------------|-------------------------|
| I love `**bold text**`.   | `<strong>bold text</strong>`     | I love **bold text**.   |
| I love `__bold text__`.   | `<strong>bold text</strong>`     | I love __bold text__.   |
| Love`**is**`bold          | `Love<strong>is</strong>bold`    | Love**is**bold.         |

---

### Italic
To italicize text, use **one asterisk (`*`)** or **one underscore (`_`)** before and after the text. 

| Markdown                | HTML                       | Rendered Output      | 
|-------------------------|----------------------------|----------------------|
| The `*cat's meow*`.     | `<em>cat's meow</em>`      | The *cat's meow*.    |
| The `_cat's meow_`.     | `<em>cat's meow</em>`      | The _cat's meow_.    |
| A`*cat*`meow            | `A<em>cat</em>meow`        | A*cat*meow.          |

---

### Bold and Italic
For text that is both bold and italic, use **three asterisks (`***`)** or **three underscores (`___`)** around the text. You can also mix and match asterisks and underscores. 

| Markdown                  | HTML                                   | Rendered Output           | 
|---------------------------|----------------------------------------|---------------------------|
| `***Important***` text.   | `<strong><em>Important</em></strong>` | ***Important*** text.     |
| `___Important___` text.   | `<strong><em>Important</em></strong>` | ___Important___ text.     |
| `__*Important*__` text.   | `<strong><em>Important</em></strong>` | __*Important*__ text.     |
| `**_Important_**` text.   | `<strong><em>Important</em></strong>` | **_Important_** text.     |
| `_**Important**_` text.   | `<em><strong>Important</strong></em>` | _**Important**_ text.     |

---

### Strikethrough
To apply strikethrough, use **double tildes (`~~`)** before and after the text.

| Markdown                | HTML                       | Rendered Output          | 
|--------------------------|----------------------------|--------------------------|
| `The world is ~~flat~~ round.` | `<p>The world is <del>flat</del> round.</p>` | The world is ~~flat~~ round. |

---

### Underline
Markdown does not natively support underlining. You can achieve it by using the HTML `<u>` tag.

| Markdown                        | HTML                          | Rendered Output               | 
|---------------------------------|------------------------------|-------------------------------|
| `<u>This sentence is underlined.</u>` | `<u>This sentence is underlined.</u>` | <u>This sentence is underlined.</u> |


### Highlight

In Markdown, there is no official syntax for highlighting text. However, you can use HTML `<mark>` tag for highlighting.

#### Example:

##### Markdown:
```
<mark>This is highlighted text</mark>
```

##### Rendered Output:
<mark>This is highlighted text</mark>

---

## Blockquotes

Blockquotes are a way to indicate that **a piece of text is a quotation** or is **being cited** from another source.

### Basic Blockquotes
To create a basic blockquote, use the `>` symbol. 

#### Example: 
##### Markdown
```markdown
> Dorothy followed her through many rooms.
```

##### HTML Conversion
```html
<blockquote>
  <p>Dorothy followed her through many rooms.</p>
</blockquote>
```

##### Rendered Output
> Dorothy followed her through many rooms.

---

### Blockquotes with Multiple Paragraphs

To include multiple paragraphs within a blockquote, add an empty line between the paragraphs. 

#### Example
##### Markdown: 
```markdown
> This is the first paragraph.
>
> And this is the second paragraph.
```

##### HTML Conversion: 

```html
<blockquote>
  <p>This is the first paragraph.</p>
  <p>And this is the second paragraph.</p>
</blockquote>
```

##### Rendered Output: 

> This is the first paragraph.  
>  
> And this is the second paragraph.

---

### Nested Blockquotes

For nested blockquotes, use multiple `>` symbols.

#### Example
##### Markdown:

```markdown
> This is the first paragraph created using `>`.
>
>> And this is the nested paragraph created using `>>`.  
>>> And this is the nested nested paragraph created using `>>>`.
```

##### HTML Conversion:

```html
<blockquote>
  <p>This is the first paragraph.</p>
  <blockquote>
    <p>And this is the nested paragraph.</p>
    <blockquote>
      <p>And this is the nested nested paragraph.</p>
    </blockquote>
  </blockquote>
</blockquote>
```

##### Rendered Ouput

> This is the first paragraph created using `>`.  
>  
>> And this is the nested paragraph created using `>>`.  
>>> And this is the nested nested paragraph created using `>>>`.

---

### Blockquotes with Other Elements

Blockquotes can include other Markdown elements, such as headers, lists, and emphasis.

#### Example
##### Markdown:
```markdown
> ##### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
> *Everything* is going **well**.
```

##### HTML Conversion:

```html
<blockquote>
  <h5>The quarterly results look great!</h5>
  <ul>
    <li>Revenue was off the chart.</li>
    <li>Profits were higher than ever.</li>
  </ul>
  <p><em>Everything</em> is going <strong>well</strong>.</p>
</blockquote>
```
##### Rendered Output:

> ##### The quarterly results look great!  
>  
> - Revenue was off the chart.  
> - Profits were higher than ever.  
>  
> *Everything* is going **well**.


---

## Lists

### Ordered List

An ordered list is created by adding a number followed by a period. A few key points:
- Always start the list with `1.`
- Numbers in the list do not need to be in sequential order.

#### Example
##### Markdown: 
```markdown
1. First item
2. Second item
3. Third item
4. Fourth item

1. First item
1. Second item
1. Third item
1. Fourth item

1. First item
3. Second item
5. Third item
12. Fourth item
```

##### HTML Conversion:

```html
<ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
  <li>Fourth item</li>
</ol>
```

##### Rendered Output:

```markdown
1. First item
2. Second item
3. Third item
4. Fourth item
```

---

### Nested List Items

To create a nested list, simply indent the list item with four spaces or a tab.

#### Example:
##### Markdown: 
```markdown
1. First item
2. Second item
3. Third item
   1. Indented item
   2. Indented item
4. Fourth item
```

##### HTML Conversion:

```html
<ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
    <ol>
      <li>Indented item</li>
      <li>Indented item</li>
    </ol>
  <li>Fourth item</li>
</ol>
```

##### Rendered Output: 

```markdown
1. First item
2. Second item
3. Third item
   1. Indented item
   2. Indented item
4. Fourth item
```

---

### Unordered List

An unordered list can be created using `*`, `-`, or `+` before the line item.

#### Example: 
##### Markdown: 

```markdown
* First item
* Second item
+ Third item
  + Indented item
- Fourth item
```

##### HTML Conversion:

```html
<ul>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
  <ul>
    <li>Indented item</li>
  </ul>
  <li>Fourth item</li>
</ul>
```

##### Rendered Output: 

```markdown
* First item
* Second item
+ Third item
  * Indented item
- Fourth item
```

---

## Inline Code 
To denote a word or phrase as code, enclose it in single backticks (\`\`).  example:

### Example: 
#### Markdown: 
```
At the command prompt, type `nano`.
```

#### Converted HTML:
```html
At the command prompt, type <code>nano</code>.
```

#### Rendered Ouput:
At the command prompt, type `nano`.

### Escaping Backticks

If your code snippet contains backticks, you can escape them by using double backticks (\`\` \`\`). 

#### Example:
##### Markdown: 

```
``Use `code` in your Markdown file.``
```
##### HTML Conversion:

```html
<code>Use `code` in your Markdown file.</code>
```

##### Rendered Output:

``Use `code` in your Markdown file.``

--- 


## Code Blocks
Code blocks can be created with indentation (not recommended) or fenced code blocks. 

### Fenced Code blocks
Fence Code Blocks in Markdown are used to display code with proper formatting and without being interpreted as regular text. These are created using triple backticks (```) or triple tildes (~~~).

~~~
```[language]
Code goes here.
```
~~~

```
~~~[language]
Code goes here.
~~~
```


#### Example: 
##### Markdown: 
~~~
```python
  print("hello world")
```
~~~

##### HTML Conversion: 
```HTML
<pre><code class="language-python">
print("hello world")
</code></pre>
```

This HTML structure uses the `<pre>` tag for preserving formatting (such as indentation and newlines) and the `<code>` tag for marking the text as code. The class="language-python" specifies the language for syntax highlighting (if supported).

##### Rendered Output: 

```python
print("hello world")
```

## Horizontal Rules
To create a horizontal rule, use three or more asterisks (***), dashes (---), or underscores (___) on a line by themselves.

| Markdown   | HTML      |
|------------|-----------|
| ***        | `<hr />`  |
| ---        | `<hr />`  |
| ___        | `<hr />`  |

***

## Links

To create a link in Markdown, enclose the link text in brackets (e.g., `[Duck Duck Go]`), followed immediately by the URL in parentheses (e.g., `(https://duckduckgo.com)`).


| Markdown | HTML Conversion | Rendered Output|
|----------|------|----------|
| ```Use [Duck Duck Go](https://duckduckgo.com).``` | `<a href="https://duckduckgo.com">Duck Duck Go</a>` | Use [Duck Duck Go](https://duckduckgo.com). |

---

### Adding Titles

To add a title that appears as a tooltip when hovering over the link, include it inside quotes right after the URL.

| Markdown | HTML Conversion | Rendered Output|
|----------|------|----------|
| `Use [Duck Duck Go](https://duckduckgo.com "My search engine!").` | `<a href="https://duckduckgo.com" title="My search engine!">Duck Duck Go</a>` | Use [Duck Duck Go](https://duckduckgo.com "My search engine!"). |

---

### URLs and Email Addresses

You can enclose URLs or email addresses in angle brackets to automatically convert them into clickable links.

| Markdown | HTML Conversion | Rendered Output|
|------------------------|-------------------------------------------------------|------------------------|
| `<https://eff.org>`     | `<a href="https://eff.org">https://eff.org</a>`        | <https://eff.org>       |
| `<fake@example.com>`   | `<a href="mailto:fake@example.com">fake@example.com</a>` | <fake@example.com>      |

---

### Formatting Links

You can add emphasis to links by wrapping them in asterisks or underscores before and after the brackets and parentheses.

| Markdown | HTML Conversion | Rendered Output|
|-----------------------------------------------|--------------------------------------------------------|-----------------------------------------------|
| `I love supporting **[EFF](https://eff.org)**.` | `<strong><a href="https://eff.org">EFF</a></strong>`    | I love supporting **[EFF](https://eff.org)**. |
| `This is the *[EFF](https://eff.org)*.`         | `<em><a href="https://eff.org">EFF</a></em>`            | This is the *[EFF](https://eff.org)*.         |

---

### Reference-Style Links

Reference-style links allow you to separate the link URLs from the text, making your Markdown cleaner and more readable. These links consist of two parts: an inline reference and a reference elsewhere in the file. You can also add an optional tooltip in quotes.

#### Example: 
##### Markdown: 
```
This is an example of a [reference-style link][example-link].

You can also add a [second link][second-link] for another reference.

[example-link]: https://www.example.com "Optional Tooltip"
[second-link]: https://www.secondexample.com
```

##### HTML Conversion: 

```html
<p>This is an example of a <a href="https://www.example.com" title="Optional Tooltip">reference-style link</a>.</p>

<p>You can also add a <a href="https://www.secondexample.com">second link</a> for another reference.</p>
```

##### Rendered Output: 

This is an example of a [reference-style link][example-link].

You can also add a [second link][second-link] for another reference.

[example-link]: https://www.example.com "Optional Tooltip"
[second-link]: https://www.secondexample.com

---


## Images

To insert an image in Markdown, start with an exclamation mark (`!`), followed by alt text in brackets, and the path or URL to the image in parentheses. Optionally, you can add a title after the URL in the parentheses.

### Example:

#### Markdown: 
```
![Fractal tree taken from Wikipedia!](https://upload.wikimedia.org/wikipedia/commons/4/4d/Fractal_canopy.svg "A fractal tree")
```

#### HTML Conversion:
```html
<img src="https://upload.wikimedia.org/wikipedia/commons/4/4d/Fractal_canopy.svg" alt="Fractal tree taken from Wikipedia!" title="A fractal tree" />
```

#### Rendered Output: 
![Fractal tree taken from Wikipedia!](https://upload.wikimedia.org/wikipedia/commons/4/4d/Fractal_canopy.svg "A fractal tree")

---

## Escaping Characters

To display a literal character that would otherwise be used to format text in a Markdown document, add a backslash `\` in front of the character.

### Example: 
#### Markdown: 
`\* Without the backslash, this would be a bullet in an unordered list.`

#### HTML Conversion: 
```html
<p>* Without the backslash, this would be a bullet in an unordered list.</p>
```

#### Rendered Output: 
\* Without the backslash, this would be a bullet in an unordered list.

### Characters You Can Escape
You can use a backslash to escape the following characters:

| Character | Name                                   |
|-----------|----------------------------------------|
| `\`      | backslash                              |
| \`  | tick mark |
| `*`       | asterisk                               |
| `_`       | underscore                             |
| `{` `}`      | curly braces                           |
| `[` `]`      | brackets                               |
| `(` `)`      | parentheses                            |
| `#`       | pound sign                             |
| `+`       | plus sign                              |
| `-`       | minus sign (hyphen)                    |
| `.`       | dot                                    |
| `!`       | exclamation mark                       |
| `\|`       | pipe|

---

## Subscript Text

In standard Markdown, there is no built-in syntax for subscript text. However, you can use **HTML** tags (`<sub>`) for subscript text.

### Example:

#### Markdown: 
```markdown
H<sub>2</sub>O
```

#### Rendered Output:
H<sub>2</sub>O

### Alternative (GitHub Flavored Markdown)
In **GitHub Flavored Markdown (GFM)**, you can use tilde (`~`) around the text for subscript:

#### Example:
##### Markdown: 
```
H~2~O
```
##### HTML Conversion:
```HTML
H<sub>2</sub>O
```
##### Rendered Output:
H~2~O

---

## Superscript Text

In standard Markdown, there is no built-in syntax for superscript text. However, you can use **HTML** tags (`<sup>`) for superscript text.

### Example:
#### Markdown: 
```
E = mc<sup>2</sup>
```

#### Rendered Output:

E = mc<sup>2</sup>

### Alternative (GitHub Flavored Markdown)
In **GitHub Flavored Markdown (GFM)**, you can use caret (`^`) around the text for superscript:

#### Example:
##### Markdown:
```
E = mc^2
```
##### HTML Conversion:
```
E = mc<sup>2</sup>
```

##### Rendered Output:
E = mc^2

---

# Extended Syntax

Markdown, as introduced by John Gruber, offers a simple and efficient way to format text. While the basic syntax is powerful, users wanted more flexibility. This led to the addition of features such as tables, code blocks, syntax highlighting, URL auto-linking, and footnotes. One of the most popular extensions is [GitHub Flavored Markdown (GFM)](https://github.github.com/gfm/).

---

## Tables

Tables allow you to present data in an organized tabular format. Below are the guidelines and examples for creating tables:

### Creating a Table
To create a table in Markdown:
1. Use three or more hyphens (`---`) to create the header row separator.
2. Separate columns with pipes (`|`).
3. Although optional, it’s recommended to add pipes at the beginning and end of each row for better readability.
4. You can include links, inline code, and text formatting (like *italic* and **bold**) in tables.
5. **Limitations**: Markdown tables don’t support features like headings, blockquotes, lists, horizontal rules, images, or raw HTML.

#### Example:

##### Markdown: 
```
| Syntax      | Description |
|-------------|-------------|
| Header      | Title       |
| Paragraph   | Text        |
```

##### HTML Conversion:
```html
<table>
  <thead>
    <tr class="header">
      <th>Syntax</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr class="odd">
      <td>Header</td>
      <td>Title</td>
    </tr>
    <tr class="even">
      <td>Paragraph</td>
      <td>Text</td>
    </tr>
  </tbody>
</table>
```

##### Rendered Output:

| Syntax      | Description |
|-------------|-------------|
| Header      | Title       |
| Paragraph   | Text        |

---

### Alignment

You can align the content of table columns by using colons (`:`) within the header row:
- `:---` for **left alignment**.
- `:---:` for **center alignment**.
- `---:` for **right alignment**.

#### Example:
##### Markdown: 

```
| Syntax      | Description   | Test Text   |
|:------------|:-------------:|------------:|
| Header      | Title         | Here's this |
| Paragraph   | Text          | And more    |
```

##### Conversion to HTML:
```html
<table>
  <thead>
    <tr class="header">
      <th style="text-align: left;">Syntax</th>
      <th style="text-align: center;">Description</th>
      <th style="text-align: right;">Test Text</th>
    </tr>
  </thead>
  <tbody>
    <tr class="odd">
      <td style="text-align: left;">Header</td>
      <td style="text-align: center;">Title</td>
      <td style="text-align: right;">Here’s this</td>
    </tr>
    <tr class="even">
      <td style="text-align: left;">Paragraph</td>
      <td style="text-align: center;">Text</td>
      <td style="text-align: right;">And more</td>---

    </tr>
  </tbody>
</table>
```

##### Rendered Output:

| Syntax      | Description   | Test Text   |
|:------------|:-------------:|------------:|
| Header      | Title         | Here's this |
| Paragraph   | Text          | And more    |

---

### Pro Tip
Creating tables manually in Markdown can be time-consuming. To speed up the process, consider using a tool like [Tables Generator](https://www.tablesgenerator.com/markdown_tables), which provides a graphical interface to create tables and automatically generates the Markdown code for you.

---

## Syntax Highlighting for Fenced Code Blocks

You can add syntax highlighting to your code by specifying the language next to the backticks (```) before the fenced code block. This helps make the code more readable by applying color highlighting based on the language used.

### Example:

#### Markdown: 
~~~
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
~~~

#### HTML Conversion:
```html
<pre>
  <code class="language-json">
    {
      &quot;firstName&quot;: &quot;John&quot;,
      &quot;lastName&quot;: &quot;Smith&quot;,
      &quot;age&quot;: 25
    }
  </code>
</pre>
```

#### Rendered Output:
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

---

## Heading IDs

In Markdown, headings automatically generate unique IDs that can be used for linking. These IDs are created by converting the heading text into a hyphen-separated, case-insensitive format.

### How It Works:
- The text of the heading becomes the ID.
- The ID is a lowercase, hyphen-separated version of the heading text.
- For example, a heading like `## Heading IDs` will generate the ID `heading-ids`.

### Example:
#### Markdown
```
## Heading IDs
```

#### HTML Conversion
```html
<h2 id="heading-ids">My Great Heading</h2>
```

### Linking to the Heading
We can link to any heading using the links markdown construct. 

### Example: 
#### Markdown
```
Link to [Heading IDs](#heading-ids)
```

#### Rendered Output:

Link to [Heading IDs](#heading-ids)

---

## Task Lists

Task lists in Markdown allow you to create a list of items with checkboxes. These checkboxes help you track progress by marking items as completed or not.

### How It Works:
- To create a task list, use dashes (`-`), asterisks (`*`), or plus signs (`+`) followed by brackets with a space (`[ ]`) to represent incomplete tasks.
- To mark a task as completed, place an `x` inside the brackets (`[x]`).

### Example:

#### Markdown:
```markdown
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
```

#### HTML Conversion: 
```html
<ul>
  <li><input type="checkbox" checked> Write the press release</li>
  <li><input type="checkbox"> Update the website</li>
  <li><input type="checkbox"> Contact the media</li>
</ul>
```

#### Rendered Output:

- [x] Write the press release  
- [ ] Update the website  
- [ ] Contact the media  

---

## Automatic URL Linking

Markdown processors automatically convert URLs into clickable links, even if you don’t wrap them in angular brackets (`< >`).

### Example:

#### Markdown:
```
https://github.com/
```

#### HTML Conversion:
```html
<a href="https://github.com/">https://github.com/</a>
```

#### Rendered Output:

[https://github.com/](https://github.com/)

---


## Disabling Automatic URL Linking

If you don’t want Markdown to automatically turn a URL into a clickable link, you can prevent it by denoting the URL as code using tick marks.

### Example:

#### Markdown:
```markdown
`https://github.com/`
```

#### HTML Conversion:
```html
<code>https://github.com/</code>
```

#### Rendered Output:

`https://github.com/`

---

## Emoji

### Using GitHub-style emoji shortcodes: 
You can use shortcodes enclosed in colons (`:`).

#### Example:
##### Markdown: 
```
:smile: :heart: :rocket:
```

##### HTMl Conversion:

```html
<span class="emoji">😀</span> <span class="emoji">❤️</span> <span class="emoji">🚀</span>
```

##### Rendered Output:

:smile: :heart: :rocket:

### Using Unicode emojis: 
You can directly insert emojis by copying and pasting the character.

#### Example:
##### Markdown: 
```markdown
😀 ❤️ 🚀
```

##### HTML Conversion:

```html
<span class="emoji">😀</span> <span class="emoji">❤️</span> <span class="emoji">🚀</span>
```

##### Rendered Output:
😀 ❤️ 🚀

---

# LaTeX Mathematical Notations

You can use LaTeX to write mathematical expressions in Markdown. Inline and block math can be easily added by enclosing expressions in dollar signs.

## Inline Math

To display math inline (within the text), enclose the expression in single dollar signs (`$`).

### Example:

#### Markdown:
```
This is an inline math expression: $E = mc^2$.
```

#### Rendered Output:
This is an inline math expression: $E = mc^2$.

---

## Block Math (Display Math)

To display math in a block format (centered and on its own line), enclose the expression in double dollar signs (`$$`).

### Example:

#### Markdown:
```
$$
\int_0^\infty x^2 \, dx
$$
```

#### Rendered Output:
$$
\int_0^\infty x^2 \, dx
$$

---


## Superscripts and Subscripts

In LaTeX, you can use superscripts (`^`) and subscripts (`_`) for mathematical expressions.

### Example:

#### Markdown:
```markdown
$x^2$  (Superscript)  
$x_1$  (Subscript)
```

#### Rendered Output:
$x^2$ (Superscript) - $x_1$ (Subscript)

---

## Fractions

To create fractions, use the LaTeX command `\frac{numerator}{denominator}`.

### Example:

#### Markdown:
```markdown
$\frac{a}{b}$
```

#### Rendered Output:
$\frac{a}{b}$

---

## Square Roots

To create square roots, use the LaTeX command `\sqrt{expression}`.

### Example:

#### Markdown:
```markdown
$\sqrt{x^2 + y^2}$
```

#### Rendered Output:
$\sqrt{x^2 + y^2}$

---

## Greek Letters

You can use LaTeX commands to display Greek letters.

### Example:

#### Markdown:
```markdown
$\alpha$, $\beta$, $\gamma$, $\delta$, $\pi$, $\theta$
```

#### Rendered Output:
$\alpha, \beta, \gamma, \delta, \pi, \theta$

---

## Summation and Product Notation

To represent summation and product notation, use `\sum` and `\prod`, respectively.

### Example:

#### Markdown:
```markdown
$\sum_{i=1}^n x_i$  (Summation)  
$\prod_{i=1}^n x_i$  (Product)
```

#### Rendered Output:
$$
\sum_{i=1}^n x_i
$$  
$$
\prod_{i=1}^n x_i
$$

---

## Limits

Use the LaTeX command `\lim` to represent limits in mathematical expressions.

### Example:

#### Markdown:
```markdown
$\lim_{x \to \infty} f(x)$
```

#### Rendered Output:
$\lim_{x \to \infty} f(x)$

$$
\lim_{x \to \infty} f(x)
$$

---

## Integral Notation

To represent integrals, use `\int`.

### Example:

#### Markdown:
```markdown
$\int_{0}^{\infty} e^{-x} dx$
```

#### Rendered Output:
$\int_{0}^{\infty} e^{-x} dx$

---

## Matrices

To create matrices, use the `\begin{matrix} ... \end{matrix}` syntax.

### Example:

#### Markdown:
```markdown
$$
\begin{matrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{matrix}
$$
```

#### Rendered Output:
$$
\begin{matrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{matrix}
$$

---

## Aligning Equations

To align equations, use the `align` environment with `&` to specify the alignment points.

### Example:

#### Markdown:
```markdown
$$
\begin{align}
  x + y &= z \\
  a + b + c &= d
\end{align}
$$
```

#### Rendered Output:
$$
\begin{align}
  x + y &= z \\
  a + b + c &= d
\end{align}
$$

---

## Exponents and Logarithms

Use `\exp` for exponentials and `\log` for logarithms.

### Example:

#### Markdown:
```markdown
$\exp(x)$  (Exponential)  
$\log(x)$  (Logarithm)
```

#### Rendered Output:
$\exp(x)$ (Exponential)  
$\log(x)$ (Logarithm)

---

## Binomial Coefficient

Use `\binom{n}{k}` for binomial coefficients.

### Example:

#### Markdown:
```markdown
$\binom{n}{k}$
```

#### Rendered Output:
$$
\binom{n}{k}
$$

---

## Brackets and Parentheses

To automatically adjust the size of brackets and parentheses, use `\left` and `\right`.

### Example:

#### Markdown:
```markdown
$\left( \frac{a}{b} \right)$
```

#### Rendered Output:
$$
\left( \frac{a}{b} \right)
$$

---

## Derivatives and Differential Operators

Use `\frac{d}{dx}` for derivatives.

### Example:

#### Markdown:
```markdown
$\frac{d}{dx} f(x)$
```

#### Rendered Output:
$$
\frac{d}{dx} f(x)
$$

---

## Angle Notations

To denote angles, use `\angle`.

### Example:

#### Markdown:
```markdown
$\angle ABC$
```

#### Rendered Output:
$$
\angle ABC
$$

---

## Vectors and Matrices

Use `\vec{}` for vectors and `\mathbf{}` for bold matrices.

### Example:

#### Markdown:
```markdown
$\vec{v}$  (Vector)  
$\mathbf{M}$  (Matrix)
```

#### Rendered Output:
$\vec{v}$ (Vector)  
$\mathbf{M}$ (Matrix)

---

## Absolute Value

To denote absolute value, use `\left| ... \right|`.

### Example:

#### Markdown:
```markdown
$\left| x \right|$
```

#### Rendered Output:
$\left| x \right|$

---

## Complex Expressions

You can combine all of these symbols to create complex mathematical expressions.

### Example:

#### Markdown:
```markdown
$$
\frac{\int_0^1 e^x \, dx}{\sqrt{1 + x^2}} + \sum_{n=0}^{\infty} \frac{1}{n!}
$$
```

#### Rendered Output:
$$
\frac{\int_0^1 e^x \, dx}{\sqrt{1 + x^2}} + \sum_{n=0}^{\infty} \frac{1}{n!}
$$

---

# LaTeX Mathematical Notations Cheat Sheet

| **Feature**               | **Syntax**                                                                 | **Rendered**                          |
|----------------------------|---------------------------------------------------------------------------|---------------------------------------|
| **Inline Math**            | `$E = mc^2$`                                                             | $E = mc^2$                            |
| **Block Math**             | `$$ \int_0^\infty x^2 \, dx $$`                                          | $\int_0^\infty x^2 \, dx$         |
| **Superscript**            | `$x^2$`                                                                  | $x^2$                                 |
| **Subscript**              | `$x_1$`                                                                  | $x_1$                                 |
| **Fraction**               | `$\frac{a}{b}$`                                                          | $\frac{a}{b}$                         |
| **Square Root**            | `$\sqrt{x^2 + y^2}$`                                                     | $\sqrt{x^2 + y^2}$                    |
| **Greek Letters**          | `$\alpha, \beta, \gamma$`                                                | $\alpha, \beta, \gamma$               |
| **Summation**              | `$\sum_{i=1}^n x_i$`                                                     | $\sum_{i=1}^n x_i$                    |
| **Limits**                 | `$\lim_{x \to \infty} f(x)$`                                             | $\lim_{x \to \infty} f(x)$            |
| **Integrals**              | `$\int_0^\infty e^{-x} dx$`                                              | $\int_0^\infty e^{-x} dx$             |
| **Matrix** | ```$$ \begin{matrix} 1 & 2 \\ 3 & 4 \end{matrix} $$```                   | $\begin{matrix} 1 & 2 \\ 3 & 4 \end{matrix}$ |
| **Exponentials**           | `$\exp(x)$`                                                              | $\exp(x)$                             |
| **Logarithms**             | `$\log(x)$`                                                              | $\log(x)$                             |
| **Binomial Coefficient**   | `$\binom{n}{k}$`                                                         | $\binom{n}{k}$                        |
| **Brackets & Parentheses** | `$\left( \frac{a}{b} \right)$`                                           | $\left( \frac{a}{b} \right)$          |
| **Derivatives**            | `$\frac{d}{dx} f(x)$`                                                    | $\frac{d}{dx} f(x)$                   |
| **Angles**                 | `$\angle ABC$`                                                           | $\angle ABC$                          |
| **Vectors**                | `$\vec{v}$`                                                              | $\vec{v}$                             |
| **Absolute Value**         | `$\left\| x \right\|$`|   $\left\| x \right\|$|
| **Complex Expression**     | ```$$ \frac{\int_0^1 e^x dx}{\sqrt{1+x^2}} + \sum_{n=0}^\infty \frac{1}{n!} $$``` | $\frac{\int_0^1 e^x dx}{\sqrt{1+x^2}} + \sum_{n=0}^\infty \frac{1}{n!}$ |
| **Aligned Equations** | ```$$\begin{align} x+y&=z \\ a+b&=c \end{align} $$``` |\_ |


$$
\begin{align} 
x+y&=z \\
a+b+c&=d
\end{align} 
$$ 

---

# Cheat Sheet

Here's the simplified table with only **Element** and **Syntax** columns:

| **Element**                    | **Syntax**                                               |
|---------------------------------|----------------------------------------------------------|
| **Heading 1**                   | `# Heading 1`                                            |
| **Heading 2**                   | `## Heading 2`                                           |
| **Heading 3**                   | `### Heading 3`                                          |
| **Heading 4**                   | `#### Heading 4`                                         |
| **Heading 5**                   | `##### Heading 5`                                        |
| **Heading 6**                   | `###### Heading 6`                                       |
| **Bold Text**                   | `**bold**` or `__bold__`                                 |
| **Italic Text**                 | `*italic*` or `_italic_`                                 |
| **Strikethrough**               | `~~strikethrough~~`                                      |
| **Ordered List**                | `1. Ordered List`                                        |
| **Unordered List**              | `- Unordered List` or `*`                               |
| **Hyperlink**                   | `[Link Text](URL)`                                       |
| **Image**                       | `![Alt Text](Image URL)`                                 |
| **Inline Code**                 | `` `code` ``                                             |
| **Code Block**                  | ` ```code``` `                                           |
| **Blockquote**                  | `> Blockquote`                                           |
| **Task List**                   | `- [ ] Task list item`                                   |
| **Escaped Characters**          | `\*emphasized\*`                                         |
| **Horizontal Rule**             | `___` or `***`                                           |
| **Emoji**                       | `:emoji:`                                                |
| **Inline Math (LaTeX)**         | `\(\math{expression}\)`                                  |
| **Block Math (LaTeX)**          | `$$\math{expression}$$`                                  |
| **Subscript**                   | `\subscript{text}`                                       |
| **Superscript**                 | `\superscript{text}`                                     |
| **Fraction (LaTeX)**            | `\frac{a}{b}`                                            |
| **Square Root (LaTeX)**         | `\sqrt{expression}`                                      |
| **Summation (LaTeX)**           | `\sum_{i=1}^n`                                          |
| **Integral (LaTeX)**            | `\int_{0}^{\infty}`                                     |
| **Limit (LaTeX)**               | `\lim_{x \to \infty}`                                   |
| **Binomial Coefficient (LaTeX)**| `\binom{n}{k}`                                          |
| **Brackets (LaTeX)**            | `\left( \frac{a}{b} \right)`                             |
| **Vector (LaTeX)**              | `\vec{v}`                                               |
| **Matrix (LaTeX)**              | `\mathbf{M}`                                            |
| **Angle (LaTeX)**               | `\angle ABC`                                            |
| **Absolute Value (LaTeX)**      | `\left| x \right|`                                      |


This table now focuses only on the **Element** and **Syntax** columns.