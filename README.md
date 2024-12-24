# The Markdown Guide - Matt Cone

# Introduction
- Markdown is a lightweight, popular, and most successful **markup language** created by John Gruber in 2004.
- Markdown is used to add formatting elements to plaintext documents. We add markdown syntax to indicate which words or phrases should look different. Eg. Heading uses \#.
- Markdown syntax is designed to be readable and unobtrusive, one can read the content before rendering.

  > The overriding design goal for Markdown's formatting syntax is to make it as readalbe as possible. The idea is that a Markdown-fomratted document should be publishable as-is, as plain text, without looking like it's been marked up with tags or formatting instructions.

- Markdown has replaced **WYSIWYG** (what you see is what you get) editors.
- It's simple (easy to learn) and powerful (to create documents, books, and technical documents).
- You can use Markdown just about anywhere, it's used for making websites, documents, notes, books, presentations, emails, and documentation.  
- Fun fact, knowing Markdown is actually a requirement in many job applications.

# How Markdown Works?
1. The text is stored in a markdown file, whose extension is `.md` or `.markdown`
2. This markdown file is fed into a **markdown application**, which contains a **markdown processor** (also referred as "parser" or an "implementation") that converts all markdown-formatted text to HTML.  
`Markdown (.md) -> Markdown application (contains Markdown Parser) -> HTML (.html)`

# Basic Syntax
* The following constructs were given by John Gurber himself. 
* `Note`: We can use HTML tags within Mardown files. 
* 
## Headings
- To create headings use \# symbol. 
- Number of \# sign corresponds to heading level.

  | Markdown            | HTML                           |
  |----------------------|--------------------------------|
  | # Heading level 1   | `<h1>Heading level 1</h1>`    |
  | ## Heading level 2  | `<h2>Heading level 2</h2>`    |
  | ### Heading level 3 | `<h3>Heading level 3</h3>`    |
  | #### Heading level 4| `<h4>Heading level 4</h4>`    |
  | ##### Heading level 5| `<h5>Heading level 5</h5>`   |
  | ###### Heading level 6| `<h6>Heading level 6</h6>`  |

- An alternate way to create heading levels 1 and 2 is by using == and -- respectively.

  ```
  Heading level 1
  ===============  
  ```
- renders as
  > Heading level 1
  > ===============  

  ```
  Heading level 2
  ---------------  
  ```
- renders as 
  > Heading level 2
  > ---------------
 
## Paragraphs
- Use a blank line to separate one or more lines of text. 

  ```Markdown
  I really like using Markdown.

  I think I'll use it from now on.
  ```

- Above gets converted to HTML as 
  ```html
  <p>I really like using Markdown.</p>

  <p>I think I'll use it from now on.</p>
  ```


## Line Breaks
- To add newline use break tag (`<br>`) or double space followed by an enter (`<space><space><enter>`).

  ```Markdown
  Newline  
  We just used line breaks.
  ```

- Becomes 
  ```html
  <p>This is the first line.<br />
  And this is the second line.</p>
  ```

## Emphasis
### Bold
- Two asterisks or underscores before and after a word or phrase. 

  | Markdown                  | HTML                                | Rendered | 
  |---------------------------|-------------------------------------| --- |
  | I love `**bold text**`.     | `<strong>bold text</strong>`       | I love **bold text** |
  | I love `__bold text__`.     | `<strong>bold text</strong>`       | I love __bold text__ |
  | Love`**is**`bold            | `Love<strong>is</strong>bold`      | Love**is**bold |

### Italic
- One asterisk or underscore before and after a word or phrase. 

  | Markdown                | HTML                          | Rendered | 
  |-------------------------|-------------------------------| --- |
  | The `*cat's meow*`.       | `<em>cat's meow</em>`        | The *cat's meow*. |
  | The `_cat's meow_`.       | `<em>cat's meow</em>`        | The _cat's meow_. |
  | A`*cat*`meow              | `A<em>cat</em>meow`          | A*cat*meow. |

### Bold and Italic
- Three asterisks or underscores before and after a word or phrase.

  | Markdown                  | HTML                                | Rendered | 
  |---------------------------|-------------------------------------| --- |
  | `***Important***` text.     | `<strong><em>Important</em></strong>` | ***Important*** text. |
  | `___Important___` text.     | `<strong><em>Important</em></strong>` | ___Important___ text. |
  | `__*Important*__` text.     | `<strong><em>Important</em></strong>` | __*Important*__ text. |
  | `**_Important_**` text.     | `<strong><em>Important</em></strong>` | **_Important_** text.  |
  | `_**Important**_` text.     | `<em><strong>Important</strong></em>` | _**Important**_ text.  |

## Blockquotes
* Blockquotes are a way to indicate that a piece of text is a quotation or is being cited from another source.

  ```
  > Dorothy followed her through many rooms. 
  ```
* gets converted to HTML as:
  ```HTML
  <blockquote>
  <p>Dorothy followed her through many rooms.</p>
  </blockquote>
  ```
* rendered as: 
  ```Markdown
  > Dorothy followed her through many rooms. 
  ```

### Blockquotes with Multiple Paragraphs
* Simply add an empty line. 
  ```
  > This the first paragraph.
  >
  > And this is the second paragraph.
  ```
* gets converted to HTML as: 
  ```HTML
  <blockquote>
  <p>This the first paragraph.</p>
  <p>And this is the second paragraph.</p>
  </blockquote>
  ```
* rendered as
  ```Markdown
  > This the first paragraph.
  >
  > And this is the second paragraph.
  ```

### Nested Blockquotes
* Use two `>>` in front of the paragraph.  
  ```
  > This the first paragraph.
  >
  >> And this is the nested paragraph.
  ```
* gets converted to HTML as: 
  ```HTML
  <blockquote>
    <p>This the first paragraph.</p>
    <blockquote>
      <p>And this is the nested paragraph.</p>
    </blockquote>
  </blockquote>
  ```
* rendered as
  
  > This the first paragraph.
  >
  >> And this is the nested paragraph.
  
### Blockquotes with Other Elements
* Can contain other Markdown elements as well, but not all. 
  ```
  > ##### The quarterly results look great!
  >
  > - Revenue was off the chart.
  > - Profits were higher than ever.
  >
  > *Everything* is going **well**.
  ```
* Converted to HTML as: 
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
* rendered as: 
  > ##### The quarterly results look great!
  >
  > - Revenue was off the chart.
  > - Profits were higher than ever.
  >
  > *Everything* is going **well**.  
  
## List
### Ordered List
* Add words after number followed by a period. 
* List should always start with 1. 
* Numbers need not be numerical order. 

  ```
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
* gets converted to HTML as: 
  
  ```html
  <ol>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
    <li>Fourth item</li>
  </ol>
  ```
* rendered as: 

  ```Markdown
  1. First item
  2. Second item
  3. Third item
  4. Fourth item
  ```

### Nested List Items
* Just indent with four spaces or a tab. 
  
  ```
  1. First item
  2. Second item
  3. Third item
  4. Fourth item
  ```
* gets converted to HTML as: 
  
  ```html
  <ol>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
    <li>Fourth item</li>
  </ol>
  ```
* rendered as: 

  ```Markdown
  1. First item
  2. Second item
  3. Third item
  4. Fourth item
  ```


## Fenced Code Blocks
- Fence Code Blocks in Markdown are used to display code with proper formatting and without being interpreted as regular text. These are created using triple backticks (```) or triple tildes (~~~).
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
- For example,
  ~~~
  ```python
    print("hello world")
  ```
  ~~~
  ```python
  print("hello world")
  ```

## Horizontal Rules
- To create a horizontal rule, use three or more asterisks (***), dashes (---), or underscores (___) on a line by themselves.

  | Markdown   | HTML      |
  |------------|-----------|
  | ***        | `<hr />`  |
  | ---        | `<hr />`  |
  | ___        | `<hr />`  |


---

## Links
- To create a link, enclose the link text in brackets (e.g., `[Duck Duck Go]`) and then follow it immediately with the URL in parentheses (e.g., `(https://duckduckgo.com)`).

  | Markdown                                | HTML                                    |
  |-----------------------------------------|-----------------------------------------|
  | Use [Duck Duck Go](https://duckduckgo.com). | `<a href="https://duckduckgo.com">Duck Duck Go</a>` |

**Rendered Output:**
Use [Duck Duck Go](https://duckduckgo.com).

### Adding Titles
- Add a title for a link that appears as a tooltip when hovered.

  | Markdown                                      | HTML                                               |
  |-----------------------------------------------|----------------------------------------------------|
  | Use [Duck Duck Go](https://duckduckgo.com "My search engine!"). | `<a href="https://duckduckgo.com" title="My search engine!">Duck Duck Go</a>` |

**Rendered Output:**
Use [Duck Duck Go](https://duckduckgo.com "My search engine!").

### URLs and Email Addresses
- Enclose URLs or email addresses in angle brackets to convert them into links.

  | Markdown                  | HTML                                    |
  |---------------------------|-----------------------------------------|
  | <https://eff.org>         | `<a href="https://eff.org">https://eff.org</a>` |
  | <fake@example.com>        | `<a href="mailto:fake@example.com">fake@example.com</a>` |

**Rendered Output:**
- [https://eff.org](https://eff.org)
- [fake@example.com](mailto:fake@example.com)

### Formatting Links
- Add emphasis to links using asterisks before and after the brackets and parentheses.

  | Markdown                                | HTML                                    |
  |-----------------------------------------|-----------------------------------------|
  | I love supporting **[EFF](https://eff.org)**. | `<strong><a href="https://eff.org">EFF</a></strong>` |
  | This is the *[EFF](https://eff.org)*.   | `<em><a href="https://eff.org">EFF</a></em>` |

**Rendered Output:**
- I love supporting **[EFF](https://eff.org)**.
- This is the *[EFF](https://eff.org)*.

### Reference-Style Links
- Use reference-style links to make URLs easier to display and read. They consist of two parts:

#### Inline Text
- The first part is formatted with two sets of brackets: one for the display text and the second for the label (case-insensitive).

  | Markdown                          | Explanation                |
  |-----------------------------------|----------------------------|
  | [hobbit-hole][1]                  | Label is `[1]`.            |
  | [hobbit-hole][A]                  | Label is `[A]`.            |

#### Reference Details
- The second part defines the label, URL, and an optional title.

  | Markdown                                      | Explanation                |
  |-----------------------------------------------|----------------------------|
  | [hobbit-hole]: https://example.com            | URL only                   |
  | [hobbit-hole]: <https://example.com> "Title" | URL with a title           |

#### Example
```markdown
In a hole in the ground there lived a hobbit. It was a [hobbit-hole][1].

[1]: <https://example.com> "Hobbit lifestyle"
```

**Rendered Output:**
In a hole in the ground there lived a hobbit. It was a [hobbit-hole](https://example.com "Hobbit lifestyle").

## Images
- To add an image, add an exclamation mark (`!`), followed by alt text in brackets, and the path or URL to the image asset in parentheses. 
- You can optionally add a title after the URL in the parentheses.

  ```markdown
  ![Philadelphia's Magic Gardens. This place was so cool!](images/philly-magic-garden.png "Philadelphia's Magic Gardens")
  ```

  ```html
  <img src="images/philly-magic-garden.png" alt="Philadelphia's Magic Gardens. This place was so cool!" title="Philadelphia's Magic Gardens" />
  ```

## Escaping Characters

- To display a literal character that would otherwise be used to format text in a Markdown document, add a backslash `\` in front of the character.

    > \* Without the backslash, this would be a bullet in an unordered list.

  ```html
  <p>* Without the backslash, this would be a bullet in an unordered list.</p>
  ```

  The rendered output looks like this:

  `* Without the backslash, this would be a bullet in an unordered list.`

### Characters You Can Escape

- You can use a backslash to escape the following characters:

  | Character | Name                                   |
  |-----------|----------------------------------------|
  | `\`      | backslash                              |
  | `` ` ``   | tick mark |
  | `*`       | asterisk                               |
  | `_`       | underscore                             |
  | `{}`      | curly braces                           |
  | `[]`      | brackets                               |
  | `()`      | parentheses                            |
  | `#`       | pound sign                             |
  | `+`       | plus sign                              |
  | `-`       | minus sign (hyphen)                    |
  | `.`       | dot                                    |
  | `!`       | exclamation mark                       |
  | `\|`       | pipe|

  Here is the content you provided converted into a Markdown file:


# Extended Syntax

## HTML

```html
<pre>
<code>
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
</code>
</pre>
```

The rendered output looks like this:

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

Need to display tick marks inside a code block? See this section to learn how to escape them.

## Syntax Highlighting

Many Markdown processors support syntax highlighting for fenced code blocks. This feature allows you to add color highlighting for whatever language your code was written in. To add syntax highlighting, specify a language next to the tick marks before the fenced code block.
~~~
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
~~~

The rendered output looks like this:

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

## Footnotes

Footnotes allow you to add notes and references without cluttering the body of the document. When you create a footnote, a superscript number with a link appears where you added the footnote reference. Readers can click the link to jump to the content of the footnote at the bottom of the page.

To create a footnote reference, add a caret and an identifier inside brackets (`[^1]`). Identifiers can be numbers or words, but they can’t contain spaces or tabs. Identifiers only correlate the footnote reference with the footnote itself — in the output, footnotes are numbered sequentially.

Add the footnote using another caret and number inside brackets with a colon and text (`[^1]: My footnote.`). You don’t have to put footnotes at the end of the document. You can put them anywhere except inside other elements like lists, block quotes, and tables.

```markdown
Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.
[^bignote]: Here's one with multiple paragraphs and code.

Indent paragraphs to include them in the footnote.

`{ my code }`

Add as many paragraphs as you like.
```

The rendered output looks like this:

Here’s a simple footnote,¹ and here’s a longer one.²

¹ This is the first footnote.  
² Here’s one with multiple paragraphs and code.  
Indent paragraphs to include them in the footnote.  
`{ my code }`  
Add as many paragraphs as you like.

## Heading IDs

Many Markdown processors support custom IDs for headings — some Markdown processors automatically add them. Adding custom IDs allows you to link directly to headings and modify them with CSS. To add a custom heading ID, enclose the custom ID in curly braces on the same line as the heading.

```markdown
### My Great Heading {#custom-id}
```

The rendered HTML output looks like this:

```html
<h3 id="custom-id">My Great Heading</h3>
```

## Linking to Heading IDs

You can link to headings with custom IDs in the file by creating a standard link with a number sign (`#`) followed by the custom heading ID.

```markdown
[Heading IDs](#heading-ids)
```

The rendered HTML output looks like this:

```html
<a href="#heading-ids">Heading IDs</a>
```

Other websites can link to the heading by adding the custom heading ID to the full URL of the webpage (e.g., [Heading IDs](https:/www.eff.org/page#heading-ids)).

## Definition Lists

Some Markdown processors allow you to create definition lists of terms and their corresponding definitions. To create a definition list, type the term on the first line. On the next line, type a colon followed by a space and the definition.

```markdown
First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.
```

The rendered output looks like this:

```
First Term  
This is the definition of the first term.

Second Term  
This is one definition of the second term.  
This is another definition of the second term.
```

## Strikethrough

You can “strikethrough” words by putting a horizontal line through the center of them. This feature allows you to indicate that certain words are a mistake not meant for inclusion in the document. To strikethrough words, use two tilde symbols (`~~`) before and after the words.

```markdown
The world is ~~flat~~ round.
```

The rendered output looks like this:

```
The world is flat round.
```

## Task Lists

Task lists allow you to create a list of items with checkboxes. In Markdown applications that support task lists, checkboxes will be displayed next to the content. To create a task list, add dashes (`-`) and brackets with a space (`[ ]`) in front of task list items. To select a checkbox, add an `x` in between the brackets (`[x]`).

```markdown
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
```

The rendered output looks like this:

- [x] Write the press release  
- [ ] Update the website  
- [ ] Contact the media  

## Automatic URL Linking

Many Markdown processors automatically turn URLs into links. That means if you type `http://www.example.com`, your Markdown processor will automatically turn it into a link even though you haven’t used brackets.

```markdown
http://example.com
```

The rendered output looks like this: http://example.com

## Disabling Automatic URL Linking

If you don’t want a URL to be automatically linked, you can remove the link by denoting the URL as code with tick marks.

```markdown
`http://www.example.com`
```

The rendered output looks like this:

```
http://www.example.com
```

This Markdown file maintains the structure and provides code blocks, footnotes, and other syntax as outlined.

Here is a Markdown cheat sheet for LaTeX mathematical notations, covering inline and display math along with various commonly used symbols and expressions:


# LaTeX Mathematical Notations in Markdown

Markdown allows you to use LaTeX-style math notations to render mathematical expressions. To use LaTeX in Markdown, enclose the math expression in dollar signs `$` for inline math and double dollar signs `$$` for block (display) math.

## 1. Inline Math
To display math inline, enclose the expression between single dollar signs (`$`).

```markdown
This is an inline math expression: $E = mc^2$.
```

Rendered:  
This is an inline math expression: \( E = mc^2 \).

## 2. Block Math (Display Math)
To display math in a block format (centered and on its own line), enclose the expression in double dollar signs (`$$`).

```markdown
$$
\int_0^\infty x^2 \, dx
$$
```

Rendered:

\[
\int_0^\infty x^2 \, dx
\]

## 3. Superscripts and Subscripts
You can use superscripts (`^`) and subscripts (`_`) in LaTeX.

```markdown
$ x^2 $  (Superscript)
$ x_1 $  (Subscript)
```

Rendered:  
\( x^2 \) (Superscript)  
\( x_1 \) (Subscript)

## 4. Fractions
Use `\frac{numerator}{denominator}` to create fractions.

```markdown
$\frac{a}{b}$
```

Rendered:  
\( $\frac{a}{b}$ \)

## 5. Square Roots
Use `\sqrt{expression}` to create square roots.

```markdown
$\sqrt{x^2 + y^2}$
```

Rendered:  
\( \sqrt{x^2 + y^2} \)

## 6. Greek Letters
You can use LaTeX commands to display Greek letters.

```markdown
$\alpha$, $\beta$, $\gamma$, $\delta$, $\pi$, $\theta$
```

Rendered:  
\( \alpha, \beta, \gamma, \delta, \pi, \theta \)

## 7. Summation and Product Notation
Use `\sum` for summation and `\prod` for product notation.

```markdown
$\sum_{i=1}^n x_i$  (Summation)
$\prod_{i=1}^n x_i$  (Product)
```

Rendered:  
\[
\sum_{i=1}^n x_i
\]  
\[
\prod_{i=1}^n x_i
\]

## 8. Limits
Use `\lim` to create limits in mathematical expressions.

```markdown
$\lim_{x \to \infty} f(x)$
```

Rendered:  
\[
\lim_{x \to \infty} f(x)
\]

## 9. Integral Notation
Use `\int` for integrals.

```markdown
$\int_{0}^{\infty} e^{-x} \, dx$
```

Rendered:  
\[
\int_{0}^{\infty} e^{-x} \, dx
\]

## 10. Matrices
You can use the `\begin{matrix} ... \end{matrix}` syntax for matrices.

```markdown
$$
\begin{matrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{matrix}
$$
```

Rendered:

\[
\begin{matrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{matrix}
\]

## 11. Aligning Equations
Use the `align` environment to align equations. Each equation is placed on a new line, and `&` is used to specify alignment points.

```markdown
$$
\begin{align}
  x + y &= z \\
  a + b &= c
\end{align}
$$
```

Rendered:

\[
\begin{align}
  x + y &= z \\
  a + b &= c
\end{align}
\]

## 12. Exponents and Logarithms
Use `\exp` for exponentials and `\log` for logarithms.

```markdown
$\exp(x)$  (Exponential)
$\log(x)$  (Logarithm)
```

Rendered:  
\( \exp(x) \) (Exponential)  
\( \log(x) \) (Logarithm)

## 13. Binomial Coefficient
Use `\binom{n}{k}` for binomial coefficients.

```markdown
$\binom{n}{k}$
```

Rendered:  
\[
\binom{n}{k}
\]

## 14. Brackets and Parentheses
You can use `\left` and `\right` to automatically adjust the size of brackets and parentheses.

```markdown
$\left( \frac{a}{b} \right)$
```

Rendered:  
\[
\left( \frac{a}{b} \right)
\]

## 15. Derivatives and Differential Operators
Use `\frac{d}{dx}` for derivatives.

```markdown
$\frac{d}{dx} f(x)$
```

Rendered:  
\[
\frac{d}{dx} f(x)
\]

## 16. Angle Notations
You can denote angles using `\angle`.

```markdown
$\angle ABC$
```

Rendered:  
\[
\angle ABC
\]

## 17. Vectors and Matrices
You can represent vectors and matrices using `\vec{}` for vectors and `\mathbf{}` for bold matrices.

```markdown
$\vec{v}$  (Vector)
$\mathbf{M}$  (Matrix)
```

Rendered:  
\( \vec{v} \) (Vector)  
\( \mathbf{M} \) (Matrix)

## 18. Absolute Value
Use `\left| ... \right|` to denote absolute value.

```markdown
$\left| x \right|$
```

Rendered:  
\[
\left| x \right|
\]

## 19. Parentheses and Brackets
Use `\left` and `\right` for automatically sized parentheses or brackets.

```markdown
$\left( \frac{a}{b} \right)$
```

Rendered:  
\[
\left( \frac{a}{b} \right)
\]

## 20. Complex Expressions
You can combine all of these symbols to create complex mathematical expressions.

```markdown
$$
\frac{\int_0^1 e^x \, dx}{\sqrt{1 + x^2}} + \sum_{n=0}^{\infty} \frac{1}{n!}
$$
```

Rendered:

\[
\frac{\int_0^1 e^x \, dx}{\sqrt{1 + x^2}} + \sum_{n=0}^{\infty} \frac{1}{n!}
\]
```

This Markdown cheat sheet provides the basic syntax and examples for using LaTeX-style math expressions within Markdown documents. You can render inline and block math, handle common operations like summations and integrals, and format equations for clarity and style.

# Markdown Cheat Sheet

## 1. Headers

Use `#` followed by a space to create headers. More `#` symbols indicate a smaller header.

```markdown
# H1 - Main Header
## H2 - Sub Header
### H3 - Sub Sub Header
#### H4 - Sub Sub Sub Header
##### H5
###### H6
```

## 2. Emphasis

### Italics
Use one asterisk `*` or underscore `_` around text to italicize.

```markdown
*Italic text* or _Italic text_
```

### Bold
Use two asterisks `**` or underscores `__` around text to make it bold.

```markdown
**Bold text** or __Bold text__
```

### Bold and Italics
Use three asterisks `***` or underscores `___` around text for bold and italic.

```markdown
***Bold and italic text*** or ___Bold and italic text___
```

## 3. Strikethrough
Use two tilde symbols `~~` to strikethrough text.

```markdown
~~Strikethrough text~~
```

## 4. Lists

### Unordered Lists
Use asterisks `*`, plus `+`, or minus `-` followed by a space.

```markdown
* Item 1
* Item 2
  * Subitem 1
  * Subitem 2
```

### Ordered Lists
Use numbers followed by a period `.`

```markdown
1. First item
2. Second item
   1. Subitem A
   2. Subitem B
```

### Task Lists
Use a dash `-` or asterisk `*` with checkboxes `[ ]`.

```markdown
- [x] Completed task
- [ ] Incomplete task
```

## 5. Links

### Inline Links
Use square brackets `[]` for the link text, followed by the URL in parentheses `()`.

```markdown
[OpenAI](https://www.openai.com/)
```

### Reference Links
You can define the URL elsewhere in the document.

```markdown
[Google]: https://www.google.com
Here is a [Google] link.
```

### Link with Title
You can also add a title for the link.

```markdown
[GitHub](https://github.com "Go to GitHub")
```

## 6. Images
Images are similar to links but with an exclamation mark `!` in front.

```markdown
![Alt Text](image-url.jpg)
```

### Image with Title
```markdown
![Alt Text](image-url.jpg "Image Title")
```

## 7. Code

### Inline Code
Use backticks `` ` `` for inline code.

```markdown
This is `inline code`.
```

### Code Blocks
Use triple backticks ```` ``` ```` or triple tildes `~~~`.

```markdown
```
Code block here
```
```

For syntax highlighting, specify the language after the backticks.

```markdown
```python
print("Hello, World!")
```
```

## 8. Blockquotes
Use the greater than symbol `>` to create blockquotes.

```markdown
> This is a blockquote.
```

### Nested Blockquotes
You can nest blockquotes by adding more `>` symbols.

```markdown
> First level
>> Second level
```

## 9. Horizontal Line
Create a horizontal line with three or more dashes `---`, asterisks `***`, or underscores `___`.

```markdown
---
```

## 10. Footnotes

You can add footnotes to your document.

```markdown
Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.
[^bignote]: Here's one with multiple paragraphs and code.

Indent paragraphs to include them in the footnote.

`{ my code }`
```

## 11. Tables

Create tables using pipes `|` and hyphens `-`.

```markdown
| Header 1 | Header 2 |
|----------|----------|
| Cell 1   | Cell 2   |
| Cell 3   | Cell 4   |
```

### Aligning Table Text

Align text within columns using colons `:`.

```markdown
| Left Aligned | Center Aligned | Right Aligned |
|:-------------|:--------------:|--------------:|
| Left text    | Center text    | Right text    |
```

## 12. Special Characters

To display special characters like `<`, `>`, `&`, etc., you need to escape them using backslashes `\`.

```markdown
\*This is not italic\*
```

## 13. HTML Elements

You can use raw HTML within Markdown. For example, for a table or custom styling.

```html
<div style="color: blue;">This is a custom div.</div>
```

## 14. Heading IDs

Add custom IDs to headings by enclosing them in curly braces `{}`.

```markdown
### My Great Heading {#custom-id}
```

### Linking to Heading IDs
Link to custom heading IDs with `#`.

```markdown
[Link to My Great Heading](#custom-id)
```

## 15. Escaping Characters

To display the special Markdown symbols like backticks or asterisks, use a backslash `\`.

```markdown
\*This will not italicize\*
```

## 16. Syntax Highlighting

For code blocks, add the language name after the opening triple backticks to enable syntax highlighting.

```markdown
```javascript
let x = 5;
console.log(x);
```
```

## 17. Definition Lists (Not Supported Everywhere)

```markdown
Term 1
: Definition of term 1

Term 2
: Definition of term 2
```

## 18. Emoji

Markdown supports emojis. Use the short code inside colons `:emoji:`.

```markdown
:smile: :heart: :rocket:
```

## 19. Comments

Markdown supports comments, but they are not rendered.

```markdown
<!-- This is a comment -->
```

## 20. HTML Entities

You can use HTML entities to display characters such as `&`, `<`, `>`, etc.

```markdown
&copy; 2024
```

## 21. Mathematical Notation (LaTeX)

Some Markdown processors support LaTeX for mathematical expressions. Use dollar signs `$` for inline math and double dollar signs `$$` for display math.

```markdown
Inline math: $E = mc^2$
Display math:
$$
\int_0^\infty x^2 dx
$$
```

## 22. Nested Lists

You can nest lists inside other lists (ordered and unordered).

```markdown
1. Item 1
   - Subitem 1
   - Subitem 2
2. Item 2
```

---

This cheat sheet covers a broad set of Markdown features, including headers, formatting, links, lists, footnotes, tables, HTML elements, and more.
```

This Markdown cheat sheet provides an extensive overview of Markdown's capabilities, including syntax highlighting, lists, tables, footnotes, and various other features. You can use this to create rich documents with Markdown!