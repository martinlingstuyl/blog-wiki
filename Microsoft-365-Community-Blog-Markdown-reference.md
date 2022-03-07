This article provides an alphabetical reference for writing Markdown for the Microsoft 365 Community Blog (the Community Blog).

[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight markup language with plain text formatting syntax. The Community Blog supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine. The Community Blog also supports custom Markdown extensions that provide richer content on the Community Blog site.

You can use any text editor to write Markdown, but we recommend [Visual Studio Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack). The Docs Authoring Pack provides editing tools and preview functionality that lets you see what your articles will look like when rendered on the Community Blog.

## Headings

We recommend using headings to create content that is easier to read and scan, but also to make content more accessible. Avoid using **bold** content where headings should be used.

Heading 1 (H1) should be reserved for the page title, and will automatically rendered via the page metadata,
but you can use any of the next 5 levels of Markdown headings:

```markdown
## This is a second-level heading (H2)

### This is a third-level heading (H3)

...

###### This is a sixth-level heading (H6)
```

- There must be a space between the last `#` and heading text.
- Each Markdown file must have one and only one H1 heading (provided by the `title` page metadata).
- HTML headings, such as `<h1>`, aren't recommended, and in some cases will cause build warnings.
- You can link to individual headings in a file via [bookmark links](how-to-write-links.md#explicit-anchor-links).
- Headings should be used to create a logical and hierarchical structure for your post. For accessibility reasons, you should only use a third-level heading inside of a second-level heading, and a fourth-level heading inside of a third-level heading, and so on. Do not skip levels.

## Emphasis

Remember that people tend to scan, rather than read online content; You can help your readers by making content more "scannable" with the use of *emphasis* in your Markdown.

To format text as **bold**, enclose it in two asterisks:

```markdown
This text is **bold**.
```

To format text as *italic*, enclose it in a single asterisk:

```markdown
This text is *italic*.
```

To format text as both ***bold and italic***, enclose it in three asterisks:

```markdown
This text is both ***bold and italic***.
```

To ~~strike text through~~, enclose it in two tildes.

```markdown
This text is ~~struck through~~ ~~striken through~~ ~~using the strike through style~~

```

<!-- 
For guidance on when to use bold and italic text, see [text formatting guidelines](text-formatting-guidelines.md). -->

Do not use emphasis where headings should be used. As a general rule, if you use emphasis on an entire line of text or an entire paragraph, *you are most likely not using emphasis correctly*.

## Links

When creating links, use the following Markdown syntax:

```markdown
[I'm an inline-style link](https://www.microsoft.com)

[I'm an inline-style link with title](https://www.microsoft.com "Microsoft Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a post on this site](../anothearticle)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself].

URLs and URLs in angle brackets will automatically get turned into links.
http://www.example.com or <http://www.example.com>.

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.microsoft.com
[1]: https://www.microsoft.com
[link text itself]: https://www.microsoft.com
```

Which produces the following links:

[I'm an inline-style link](https://www.microsoft.com)

[I'm an inline-style link with title](https://www.microsoft.com "Microsoft Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a post on this site](../anothearticle)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself].

URLs and URLs in angle brackets will automatically get turned into links.
http://www.example.com or <http://www.example.com>.

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.microsoft.com
[1]: https://www.microsoft.com
[link text itself]: https://www.microsoft.com

We'll cover more later, but here is a very preliminary checklist:

- Do not use terms like **here** and **this** in your links; remember that people who use screen readers often skip directly to navigating through the links on your page, and if they all say *here*, *here*, *here*, your audience won't understand the context of the link.
- If pointing to a Microsoft URL, remove the language/locale-specific segment of the URL (e.g. `/en-us/`) and replace it with a single forward slash (`/`); remember that this is a global community, and that everyone should be able to read the content in the language of their choice.
- All links should use `https://`

<!--
For information on syntax for links, see [Use links in documentation](how-to-write-links.md). -->

## Paragraph

Use paragraphs to create content that is easier to break down into separate ideas, and to make the page easier to read and/or scan.

Remember that you need a blank line between sentences, or they will be grouped together on the page.

For example, the following Markdown code:

```markdown
Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam nihil enim maxime corporis cumque totam aliquid nam sint inventore optio modi neque laborum officiis necessitatibus, facilis placeat pariatur! Voluptatem, sed harum pariatur adipisci voluptates voluptatum cumque, porro sint minima similique magni perferendis fuga! Optio vel ipsum excepturi tempore reiciendis id quidem? Vel in, doloribus debitis nesciunt fugit sequi magnam accusantium modi neque quis, vitae velit, pariatur harum autem a! Velit impedit atque maiores animi possimus asperiores natus repellendus excepturi sint architecto eligendi non, omnis nihil. Facilis, doloremque illum. Fugit optio laborum minus debitis natus illo perspiciatis corporis voluptatum rerum laboriosam.
Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam nihil enim maxime corporis cumque totam aliquid nam sint inventore optio modi neque laborum officiis necessitatibus, facilis placeat pariatur! Voluptatem, sed harum pariatur adipisci voluptates voluptatum cumque, porro sint minima similique magni perferendis fuga! Optio vel ipsum excepturi tempore reiciendis id quidem? Vel in, doloribus debitis nesciunt fugit sequi magnam accusantium modi neque quis, vitae velit, pariatur harum autem a! Velit impedit atque maiores animi possimus asperiores natus repellendus excepturi sint architecto eligendi non, omnis nihil. Facilis, doloremque illum. Fugit optio laborum minus debitis natus illo perspiciatis corporis voluptatum rerum laboriosam.
Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam nihil enim maxime corporis cumque totam aliquid nam sint inventore optio modi neque laborum officiis necessitatibus, facilis placeat pariatur! Voluptatem, sed harum pariatur adipisci voluptates voluptatum cumque, porro sint minima similique magni perferendis fuga! Optio vel ipsum excepturi tempore reiciendis id quidem? Vel in, doloribus debitis nesciunt fugit sequi magnam accusantium modi neque quis, vitae velit, pariatur harum autem a! Velit impedit atque maiores animi possimus asperiores natus repellendus excepturi sint architecto eligendi non, omnis nihil. Facilis, doloremque illum. Fugit optio laborum minus debitis natus illo perspiciatis corporis voluptatum rerum laboriosam.

```

Will produce the following run-on paragraph because there are no blank lines between each paragraph.

---

Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam nihil enim maxime corporis cumque totam aliquid nam sint inventore optio modi neque laborum officiis necessitatibus, facilis placeat pariatur! Voluptatem, sed harum pariatur adipisci voluptates voluptatum cumque, porro sint minima similique magni perferendis fuga! Optio vel ipsum excepturi tempore reiciendis id quidem? Vel in, doloribus debitis nesciunt fugit sequi magnam accusantium modi neque quis, vitae velit, pariatur harum autem a! Velit impedit atque maiores animi possimus asperiores natus repellendus excepturi sint architecto eligendi non, omnis nihil. Facilis, doloremque illum. Fugit optio laborum minus debitis natus illo perspiciatis corporis voluptatum rerum laboriosam.
Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam nihil enim maxime corporis cumque totam aliquid nam sint inventore optio modi neque laborum officiis necessitatibus, facilis placeat pariatur! Voluptatem, sed harum pariatur adipisci voluptates voluptatum cumque, porro sint minima similique magni perferendis fuga! Optio vel ipsum excepturi tempore reiciendis id quidem? Vel in, doloribus debitis nesciunt fugit sequi magnam accusantium modi neque quis, vitae velit, pariatur harum autem a! Velit impedit atque maiores animi possimus asperiores natus repellendus excepturi sint architecto eligendi non, omnis nihil. Facilis, doloremque illum. Fugit optio laborum minus debitis natus illo perspiciatis corporis voluptatum rerum laboriosam.
Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam nihil enim maxime corporis cumque totam aliquid nam sint inventore optio modi neque laborum officiis necessitatibus, facilis placeat pariatur! Voluptatem, sed harum pariatur adipisci voluptates voluptatum cumque, porro sint minima similique magni perferendis fuga! Optio vel ipsum excepturi tempore reiciendis id quidem? Vel in, doloribus debitis nesciunt fugit sequi magnam accusantium modi neque quis, vitae velit, pariatur harum autem a! Velit impedit atque maiores animi possimus asperiores natus repellendus excepturi sint architecto eligendi non, omnis nihil. Facilis, doloremque illum. Fugit optio laborum minus debitis natus illo perspiciatis corporis voluptatum rerum laboriosam.

---


## Alerts (Note, Tip, Important, Caution, Warning)

Alerts are a Markdown extension to create block quotes that render on the Community Blog with colors and icons that indicate the significance of the content.

Avoid notes, tips, and important boxes. Readers tend to skip over them. It's better to put that info directly into the article text.

If you need to use alerts, limit them to one or two per article. Multiple notes should never be next to each other in an article.

The following alert types are supported:

```markdown
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

These alerts look like this on the Community Blog:

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.


## Angle brackets

If you use angle brackets in text in your file (for example, to denote a placeholder), you need to manually encode the angle brackets. Otherwise, Markdown thinks that they're intended to be an HTML tag.

For example, encode `<script name>` as `&lt;script name&gt;` or `\<script name>`.

Angle brackets don't have to be escaped in text formatted as inline code or in code blocks.

## Apostrophes and quotation marks

If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks. These need to be encoded or changed to basic apostrophes or quotation marks. Otherwise, you end up with things like this when the file is published: Itâ&euro;&trade;s

Here are the encodings for the "smart" versions of these punctuation marks:

- Left (opening) quotation mark: `&#8220;`
- Right (closing) quotation mark: `&#8221;`
- Right (closing) single quotation mark or apostrophe: `&#8217;`
- Left (opening) single quotation mark (rarely used): `&#8216;`

> **TIP:** To avoid "smart" characters in your Markdown files, rely on the Docs Authoring Pack's smart quote replacement feature. 

<!-- For more information, see [smart quote replacement](docs-authoring/smart-quote-replacement.md). -->

## Blockquotes

Blockquotes are created using the `>` character:

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

The preceding example renders as follows:

> This is a blockquote. It is usually rendered indented and with a different background color.


## Code snippets

The Community Blog Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences. 

Inline `code` is enclosed in backticks (\`).


Code blocks should be delimited with three backticks (\`\`\`) before and after the code block. To automatically provide syntax highlighting, make sure to specify the language of the code block immediately after the opening \`\`\`.

```markdown
    ```javascript
    var s = "JavaScript syntax highlighting";
    alert(s);
    ```
     
    ```python
    s = "Python syntax highlighting"
    print s
    ```
```

Will produce the following:

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 
```python
s = "Python syntax highlighting"
print s
```
<!-- 
For more information, see [How to add code to docs](code-in-docs.md). -->

## Comments

The Community Blog supports HTML comments if you must comment out sections of your article:

```
<!--- Here's my comment --->
```

> **WARNING:** Do not put private or sensitive information in HTML comments. The Community Blog carries HTML comments through to the published HTML that goes public. While HTML comments are invisible to the reader's eye, they are exposed in the HTML underneath.


## HTML

Although Markdown supports inline HTML, HTML isn't recommended for publishing to the Community Blog, and except for a limited list of values will cause build errors or warnings.

## Images

The following file types are supported by default for images:

- `.jpg`
- `.png`
- `.gif`

To embed an image, use the following syntax:

```markdown
{{< image alt="DESCRIBE THE IMAGE" src="images/blog/your-unique-article-name/blog-3.jpg" >}}
```

And place your images in a new folder matching your article name, under this path `assets\images\blog\your-unique-article-name`.

While you can use the traditional Markdown syntax for images, the syntax we use will cause the image to be optimized for various device resolutions, ensuring to your readers get the fastest browsing experience possible.

Important image tips:

- Always provide an alternate text describing the image. Alternate text is required for screen readers for the visually impaired. It's also useful if there's a site bug where the image can't render. Your article will not be published if you do not provide one.
- Do not point to an external image, always upload a high-resolution image.

## Indentation

In Markdown, spaces before the first character of a line determine the line's alignment relative to the preceding lines. Indentation especially influences numbered and bulleted lists to render multiple levels of nesting in a hierarchical or outline format.

To indent text to align with a preceding paragraph or an item in a numbered or bulleted list, use spaces.

The following two examples show how indented paragraphs render based on their relationship to other paragraphs.

```
1. This is a numbered list example (one space after the period before the letter T).
   This sentence is indented three spaces.
   This code block is indented three spaces.

- This is a bulleted list example (one space after the bullet before the letter T).
  This sentence is indented two spaces.
  > [!TIP]
  > This tip is indented two spaces.
  - This is a second-level bullet (indented two spaces, with one space after the bullet before the letter T).
    This sentence is indented four spaces.
    > This quote block is indented four spaces.
```

The example above renders as:

1. This is a numbered list example (one space after the period before the letter T).

   This sentence is indented three spaces.

   ```
   This code block is indented three spaces.
   ```

- This is a bulleted list example (one space after the bullet before the letter T).

  This sentence is indented two spaces.

  > [!TIP]
  > This tip is indented two spaces.
  - This is a second-level bullet (indented two spaces, with one space after the bullet before the letter T).

    This sentence is indented four spaces.

    > This quote block is indented four spaces.


## Lists (Numbered, Bulleted, Checklist)

### Numbered list

To create a numbered list, you can use all 1s. The numbers are rendered in ascending order as a sequential list when published. For increased source readability, you can increment your lists manually.

Don't use letters in lists, including nested lists. They don't render correctly when published to the Community Blog. Nested lists using numbers will render as lowercase letters when published. For example:

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

This renders as follows:

1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)

### Bulleted list

To create a bulleted list, use `-` or `*` followed by a space at the beginning of each line:

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

This renders as follows:

- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!

Whichever syntax you use, `-` or `*`, use it consistently within an article.

### Checklist

Checklists are available for use on the Community Blog via a custom Markdown extension:

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

This example renders on the Community Blog like this:

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content. Do not add random checklists throughout your articles.


## Subscript and superscript

You should only use subscript or superscript when necessary for technical accuracy, such as when writing about mathematical formulas. Don't use them for non-standard styles, such as footnotes.

For both subscript and superscript, use HTML:

```html
Hello <sub>This is subscript!</sub>
```

This renders as follows:

Hello <sub>This is subscript!</sub>

```html
Goodbye <sup>This is superscript!</sup>
```

This renders as follows:

Goodbye <sup>This is superscript!</sup>

## Tables

The simplest way to create a table in Markdown is to use pipes and lines. To create a standard table with a header, follow the first line with dashed line:

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

This renders as follows:

|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|

You can align the columns by using colons:

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

Renders as follows:

| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

> [!TIP]
> The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!
>
> You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).


### Data matrix tables

A data matrix table has both a header and a weighted first column, creating a matrix with an empty cell in the top left. The Community Blog has custom Markdown for data matrix tables:

```md
|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |
```

The example renders as:

|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |

Every entry in the first column must be styled as bold (`**bold**`); otherwise the tables won't be accessible for screen readers or valid for the Community Blog.

> **TIP:** The Docs Authoring Pack for VS Code includes a function to convert a regular Markdown table into a data matrix table. Just select the table, right-click, and select **Convert to data matrix table**.

### HTML Tables

HTML tables aren't recommended for the Community Blog. They aren't human readable in the source - which is a key principle of Markdown.
