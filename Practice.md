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

### Strikethrough
* Putting a horizontal line through the center of them. 
* Use double tilde (~~) before and after the words
  
  ```
  The world is ~~flat~~ round. 
  ```

* get converted to html as: 
  ```html
  <p>The world is <del>flat</del> round.</p>
  ```
* rendered output as: 
  
  The world is ~~flat~~ round. 


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

  ```Markdown
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
     1. Indented item
     2. Indented item
  4. Fourth item
  ```
* gets converted to HTML as: 
  
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
* rendered as: 

  ```Markdown
  1. First item
  2. Second item
  3. Third item
     1. Indented item
     2. Indented item
  4. Fourth item
  ```
### Unordered List
* Can be created using `*` or `-` or `+` in front of line items. 

  ```Markdown
  * First item
  * Second item
  + Third item
    + Indented item
  - Fourth item
  ```

* gets converted to HTML as: 
  
  ```html
  <ul>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
    <ul>
      <li>Indented item</li>
    <ul>
    <li>Fourth item</li>
  </ul>
  ```
* rendered as: 

  > * First item
  > * Second item
  > + Third item
  >   * Indented item
  > - Fourth item

### Adding Elements in Lists
* Add one or more elements to list, using indentation.

## Code
* To denote word or phrase as code, enclose it in tick marks (\`).

  ```
  At the command prompt, type `nano`.
  ```
* gets converted to HTML as: 
  ```html
  At the command prompt, type <code>nano</code>
  ```
* rendered as: 
  ```Markdown
  At the command prompt, type `nano`.
  ```

### Escaping Tick Marks
* If the segment you want denote as code contains tick marks, use double tick marks. 
  ```
  ``Use `code` in your Markdown file.``
  ```
* get converted to HTML as:
  ```html
  <code>Use `code` in your Markdown file.</code>
  ```
* rendered as: 
  ``Use `code` in your Markdown file.``

## Code Blocks
* Code blocks can be created with indentation (not recommended) or fenced code blocks. 
### Fenced Code blocks
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
* get rendered as

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
- Enclose the link text in brackets (e.g., `[Duck Duck Go]`) and then follow it immediately with the URL in parentheses (e.g., `(https://duckduckgo.com)`).

  | Markdown| HTML| Rendered |
  | --- | --- | --- |
  | ```Use [Duck Duck Go](https://duckduckgo.com).``` | `<a href="https://duckduckgo.com">Duck Duck Go</a>` | Use [Duck Duck Go](https://duckduckgo.com).|



### Adding Titles
- Add a title for a link that appears as a tooltip when hovered.

  | Markdown| HTML | Rendered |
  | --- | --- | --- |
  | `Use [Duck Duck Go](https://duckduckgo.com "My search engine!").` | `<a href="https://duckduckgo.com" title="My search engine!">Duck Duck Go</a>` | Use [Duck Duck Go](https://duckduckgo.com "My search engine!"). |

### URLs and Email Addresses
- Enclose URLs or email addresses in angle brackets to convert them into links.

  | Markdown    | HTML  | Rendered |
  |---|---| --- |
  | `<https://eff.org>` | `<a href="https://eff.org">https://eff.org</a>` | <https://eff.org> |
  | `<fake@example.com>` | `<a href="mailto:fake@example.com">fake@example.com</a>` | <fake@example.com> |


### Formatting Links
- Add emphasis to links using asterisks before and after the brackets and parentheses.

  | Markdown | HTML  | Rendered |
  |---|---| --- |
  | `I love supporting **[EFF](https://eff.org)**.` | `<strong><a href="https://eff.org">EFF</a></strong>` | I love supporting **[EFF](https://eff.org)**. |
  | `This is the *[EFF](https://eff.org)*.`   | `<em><a href="https://eff.org">EFF</a></em>` | This is the *[EFF](https://eff.org)*. |

### Reference-Style Links
- Reference-style links in Markdown allow you to keep the link URLs separate from the text. 
- This makes the text cleaner and more readable. 
- They contain two parts, inline mention and reference elsewhere in the Markdown file. 
- Can add an optional tooltip in quotes.
- Here's an example:

  ```
  This is an example of a [reference-style link][example-link].

  You can also add a [second link][second-link] for another reference.

  [example-link]: https://www.example.com "Optional Tooltip"
  [second-link]: https://www.secondexample.com
  ```

* When rendered: 
  
  This is an example of a [reference-style link][example-link].

  You can also add a [second link][second-link] for another reference.

  [example-link]: https://www.example.com "Optional Tooltip"
  [second-link]: https://www.secondexample.com


## Images
- Add an exclamation mark (`!`), followed by alt text in brackets, and the path or URL to the image asset in parentheses. 
- You can optionally add a title after the URL in the parentheses.

  ```markdown
  ![Philadelphia's Magic Gardens. This place was so cool!](images/philly-magic-garden.png "Philadelphia's Magic Gardens")
  ```
- gets converted to HTML as: 
  
  ```html
  <img src="images/philly-magic-garden.png" alt="Philadelphia's Magic Gardens. This place was so cool!" title="Philadelphia's Magic Gardens" />
  ```

## Escaping Characters

- To display a literal character that would otherwise be used to format text in a Markdown document, add a backslash `\` in front of the character.

  `\* Without the backslash, this would be a bullet in an unordered list.`
* gets converted to HTML as: 

  ```html
  <p>* Without the backslash, this would be a bullet in an unordered list.</p>
  ```

  The rendered output looks like this:

  \* Without the backslash, this would be a bullet in an unordered list.

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

---

# Extended Syntax
* Whatever we have seen so far is was introduced by John Gruber himself. 
* Although powerful, people wanted more. 
* Hence we have constructs for tables, code blocks, syntax highlighting, URL auto-linking, and footnotes. 
* A popular one is [GitHub Flavored Markdown (GFM)](https://github.github.com/gfm/)

## Table
* Use three or more hypens to create column header.
* Use pipes | to spearate each column.
* Adding pipes at either end of table is optional, but is recommended. 
* Table can have links, code words, and emphasis. 
* Table cannot have headings, blockquotes, lists, horizontal rules, imaegs, or HTML tags.
* Creating tables using markdown format can be tedious, instead you can use [Tables Generator](https://www.tablesgenerator.com/markdown_tables), that takes GUI input and renders Markdown-formatted text table.

  ```
  | Syntax | Description |
  | --- | ------ |
  | Header | Title |
  | Paragraph | Text |
  ```
* get converted to html as: 

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
* gets rendered as: 
  | Syntax | Description |
  | --- | ------ |
  | Header | Title |
  | Paragraph | Text |

### Alignment
* Use colon (:) to left, right, or on both side of the hypens within header row.
  ```
  | Syntax | Description | Test Text |
  | :--- | :------: | ---: | 
  | Header | Title | Here's this |
  | Paragraph | Text | And more |
  ```
* get converted to html as: 

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
        <td style="text-align: right;">And more</td>
      </tr>
    </tbody>
  </table>
  ```
* gets rendered as: 
  | Syntax | Description | Test Text |
  | :--- | :------: | ---: | 
  | Header | Title | Here's this |
  | Paragraph | Text | And more |

## Fenced Code Blocks
* You can use three ticks \`\`\` or three tildes \~\~\~, before and after the code block.

  ```
  {
    "firstName": "John",
    "lastName": "Smith",
    "age": 25
  }
  ```
* gets converted to HTML as: 
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

* The rendered output looks like this:
  ```
  {
    "firstName": "John",
    "lastName": "Smith",
    "age": 25
  }
  ```

## Syntax Highlighting
* To add color highlighting for whatever language your code was written in. 
* Specify a language next to the tick marks before the fenced code block.
  ~~~
  ```json
  {
    "firstName": "John",
    "lastName": "Smith",
    "age": 25
  }
  ```
  ~~~
* gets converted to json as: 
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
* rendered as:

  ```json
  {
    "firstName": "John",
    "lastName": "Smith",
    "age": 25
  }
  ```
## Heading IDs

* The name itself becomes an id. 
* The id is hypen separated and case insensitive representation of heading. 
* `## Heading IDs` will have identifier as `heading-ids`, and can be referenced from anywhere. 
* For example 
  ```
  ### My Great Heading 
  ```

* converted to HTML as:

  ```html
  <h3 id="my-great-heading">My Great Heading</h3>
  ```

* You can now link to this section using `Link to [My Great Heading](#my-great-heading)`.

* rendered as: 
  ### My Great Heading

  Link to [My Great Heading](#my-great-heading)

## Task Lists
* Used to create a list of items with checkboxes. 
* Checkboxes will be displayed next to the content. 
* To create a task list, add dashes (`-`) and brackets with a space (`[ ]`) in front of task list items. 
* To select a checkbox, add an `x` in between the brackets (`[x]`).

  ```
  - [x] Write the press release
  * [ ] Update the website
  + [ ] Contact the media
  ```

* rendered as:

  - [x] Write the press release  
  * [ ] Update the website  
  + [ ] Contact the media  

## Automatic URL Linking

* Many Markdown processors automatically turn URLs into links even though you haven’t used angular brackets.

  ```
  http://example.com
  ```
* gets converted to HTML as: 
  
  ```html
  <a href="http://example.com">http://example.com</a>
  ```
* rendered as: 
 
  http://example.com

## Disabling Automatic URL Linking

* You can remove the link by denoting the URL as code with tick marks.

  ```
  `http://www.example.com`
  ```
* gets converted to HTML as: 

  ```html
  <code>http://www.example.com</code>
  ```

* rendered as:
  ```
  http://www.example.com
  ```

# LaTeX Mathematical Notations in Markdown

* To use LaTeX in Markdown, enclose the math expression in dollar signs `$` for inline math and double dollar signs `$$` for block (display) math.

## 1. Inline Math
* To display math inline, enclose the expression between single dollar signs (`$`).

  ```markdown
  This is an inline math expression: $E = mc^2$.
  ```

* Rendered as:  
  This is an inline math expression: $E = mc^2$.

## 2. Block Math (Display Math)
* To display math in a block format (centered and on its own line), enclose the expression in double dollar signs (`$$`).

  ```markdown
  $$
  \int_0^\infty x^2 \, dx
  $$
  ```

* Rendered as:

  $$
  \int_0^\infty x^2 \, dx
  $$

## 3. Superscripts and Subscripts
* You can use superscripts (`^`) and subscripts (`_`) in LaTeX.

  ```markdown
  $x^2$  (Superscript)
  $x_1$  (Subscript)
  ```

* Rendered as: $x^2$ (Superscript) - $x_1$ (Subscript)

## 4. Fractions
* Use `\frac{numerator}{denominator}` to create fractions.

  ```markdown
  $\frac{a}{b}$
  ```

* Rendered as: $\frac{a}{b}$

## 5. Square Roots
* Use `\sqrt{expression}` to create square roots.

  ```markdown
  $\sqrt{x^2 + y^2}$
  ```

* Rendered as: 
$\sqrt{x^2 + y^2}$

## 6. Greek Letters
* You can use LaTeX commands to display Greek letters.

  ```markdown
  $\alpha$, $\beta$, $\gamma$, $\delta$, $\pi$, $\theta$
  ```

* Rendered as: $\alpha, \beta, \gamma, \delta, \pi, \theta$

## 7. Summation and Product Notation
* Use `\sum` for summation and `\prod` for product notation.

  ```markdown
  $\sum_{i=1}^n x_i$  (Summation)
  $\prod_{i=1}^n x_i$  (Product)
  ```

* Rendered as: 
$$
\sum_{i=1}^n x_i
$$  
$$
\prod_{i=1}^n x_i
$$

## 8. Limits
* Use `\lim` to create limits in mathematical expressions.

  ```markdown
  $\lim_{x \to \infty} f(x)$
  ```

* Rendered as: 
$\lim_{x \to \infty} f(x)$
$$\lim_{x \to \infty} f(x)$$


## 9. Integral Notation
* Use `\int` for integrals.

```markdown
$\int_{0}^{\infty} e^{-x} dx$
```

* Rendered as: 
$\int_{0}^{\infty} e^{-x} dx$

## 10. Matrices
* You can use the `\begin{matrix} ... \end{matrix}` syntax for matrices.

  ```markdown
  $$
  \begin{matrix}
  1 & 2 & 3 \\
  4 & 5 & 6 \\
  7 & 8 & 9
  \end{matrix}
  $$
  ```

* Rendered as:

$$
\begin{matrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{matrix}
$$

## 11. Aligning Equations
* Use the `align` environment to align equations. 
* Each equation is placed on a new line, and `&` is used to specify alignment points.

  ```markdown
  $$
  \begin{align}
    x + y &= z \\
    a + b + c &= c
  \end{align}
  $$
  ```

* Rendered as:

$$
\begin{align}
  x + y &= z \\
  a + b + c&= c
\end{align}
$$

## 12. Exponents and Logarithms
* Use `\exp` for exponentials and `\log` for logarithms.

  ```markdown
  $\exp(x)$  (Exponential)
  $\log(x)$  (Logarithm)
  ```

* Rendered as: 
    
  $\exp(x)$ (Exponential)  
  $\log(x)$ (Logarithm)

## 13. Binomial Coefficient
* Use `\binom{n}{k}` for binomial coefficients.

  ```markdown
  $\binom{n}{k}$
  ```

* Rendered as: 
$$
\binom{n}{k}
$$

## 14. Brackets and Parentheses
* You can use `\left` and `\right` to automatically adjust the size of brackets and parentheses.

  ```markdown
  $\left( \frac{a}{b} \right)$
  ```

* Rendered as: 
$$
\left( \frac{a}{b} \right)
$$

## 15. Derivatives and Differential Operators
* Use `\frac{d}{dx}` for derivatives.

  ```markdown
  $\frac{d}{dx} f(x)$
  ```

* Rendered as: 
$$
\frac{d}{dx} f(x)
$$

## 16. Angle Notations
* You can denote angles using `\angle`.

  ```markdown
  $\angle ABC$
  ```

* Rendered as: 
$$
\angle ABC
$$

## 17. Vectors and Matrices
* You can represent vectors and matrices using `\vec{}` for vectors and `\mathbf{}` for bold matrices.

  ```markdown
  $\vec{v}$  (Vector)
  $\mathbf{M}$  (Matrix)
  ```

* Rendered as: 
  
  $\vec{v}$ (Vector)  
  $\mathbf{M}$ (Matrix)

## 18. Absolute Value
* Use `\left| ... \right|` to denote absolute value.

  ```markdown
  $\left| x \right|$
  ```

* Rendered as: 
$\left| x \right|$

## 19. Complex Expressions
* You can combine all of these symbols to create complex mathematical expressions.

  ```markdown
  $$
  \frac{\int_0^1 e^x \, dx}{\sqrt{1 + x^2}} + \sum_{n=0}^{\infty} \frac{1}{n!}
  $$
  ```

* Rendered as:

$$
\frac{\int_0^1 e^x \, dx}{\sqrt{1 + x^2}} + \sum_{n=0}^{\infty} \frac{1}{n!}
$$

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
a+b+c&=c
\end{align} 
$$ 

