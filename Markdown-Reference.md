# Microsoft 365 Community Blog Markdown reference

This article provides an alphabetical reference for writing Markdown for the Microsoft 365 Community Blog.

[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight markup language with plain text formatting syntax. Community Blog supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine. Community Blog also supports custom Markdown extensions that provide richer content on the Community Blog site.

You can use any text editor to write Markdown, but we recommend [Visual Studio Code](https://code.visualstudio.com/) with the [Community Blog Authoring Pack](https://aka.ms/DocsAuthoringPack). The Community Blog Authoring Pack provides editing tools and preview functionality that lets you see what your articles will look like when rendered on Community Blog.

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

Remember that people tend to scan, rather than read online content; You can help your readers by making content more "scannable" with the use of emphasis in your markdown.

Consider using the following emphasis formats:

- Emphasis, aka italics, with *asterisks* or _underscores_ (`*asterisks*` or `_underscores_`).
- 
- Strong emphasis, aka bold, with **asterisks** or __underscores__ (`**asterisks**` or `__underscores__`).
- 
- Combined emphasis with **asterisks and _underscores_** (`**asterisks and _underscores_**`).
- 
- Strikethrough uses two tildes. ~~Scratch this.~~ (`~~Scratch this.~~`)

Do not use emphasis where headings should be used. As a general rule, if you use emphasis on an entire line of text or an entire paragraph, *you are most likely not using emphasis correctly*.

## Links

When creating links, use the following Markdown syntax:

```markdown
[I'm an inline-style link](https://www.microsoft.com)

[I'm an inline-style link with title](https://www.microsoft.com "Microsoft Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a file in this repository](../blob/main/LICENSE)

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

[I'm a relative reference to a file in this repository](../blob/main/LICENSE)

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

Will produce the following run-on paragraph because the lines between each paragraph were not blank -- they contained a single whitespace.

---
Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam nihil enim maxime corporis cumque totam aliquid nam sint inventore optio modi neque laborum officiis necessitatibus, facilis placeat pariatur! Voluptatem, sed harum pariatur adipisci voluptates voluptatum cumque, porro sint minima similique magni perferendis fuga! Optio vel ipsum excepturi tempore reiciendis id quidem? Vel in, doloribus debitis nesciunt fugit sequi magnam accusantium modi neque quis, vitae velit, pariatur harum autem a! Velit impedit atque maiores animi possimus asperiores natus repellendus excepturi sint architecto eligendi non, omnis nihil. Facilis, doloremque illum. Fugit optio laborum minus debitis natus illo perspiciatis corporis voluptatum rerum laboriosam.
 
Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam nihil enim maxime corporis cumque totam aliquid nam sint inventore optio modi neque laborum officiis necessitatibus, facilis placeat pariatur! Voluptatem, sed harum pariatur adipisci voluptates voluptatum cumque, porro sint minima similique magni perferendis fuga! Optio vel ipsum excepturi tempore reiciendis id quidem? Vel in, doloribus debitis nesciunt fugit sequi magnam accusantium modi neque quis, vitae velit, pariatur harum autem a! Velit impedit atque maiores animi possimus asperiores natus repellendus excepturi sint architecto eligendi non, omnis nihil. Facilis, doloremque illum. Fugit optio laborum minus debitis natus illo perspiciatis corporis voluptatum rerum laboriosam.
 
 
 
 
Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam nihil enim maxime corporis cumque totam aliquid nam sint inventore optio modi neque laborum officiis necessitatibus, facilis placeat pariatur! Voluptatem, sed harum pariatur adipisci voluptates voluptatum cumque, porro sint minima similique magni perferendis fuga! Optio vel ipsum excepturi tempore reiciendis id quidem? Vel in, doloribus debitis nesciunt fugit sequi magnam accusantium modi neque quis, vitae velit, pariatur harum autem a! Velit impedit atque maiores animi possimus asperiores natus repellendus excepturi sint architecto eligendi non, omnis nihil. Facilis, doloremque illum. Fugit optio laborum minus debitis natus illo perspiciatis corporis voluptatum rerum laboriosam. 
---