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
