[Home/Inicio](README.md) · [Versión en español](guia-markdown-es.md)

---

# Basic Markdown Guide <!-- omit from toc -->

## Syntax, organization, and examples <!-- omit from toc -->

**Author:** Gonzalo Fernández Romero

**Purpose:** Technical documentation and writing

**Creation date:** July 2026

**Last updated:** July 2026

---

## Introduction <!-- omit from toc -->

Markdown is a lightweight markup language used to write structured documents. This guide covers the essential features needed to:

- Take notes.
- Document programs.
- Prepare content for GitHub.
- Write formulas or include code.

## Table of Contents <!-- omit from toc -->


- [1. Headings and sections](#1-headings-and-sections)
- [2. Text formatting](#2-text-formatting)
  - [Bold](#bold)
  - [Italic](#italic)
  - [Bold and italic](#bold-and-italic)
- [3. Paragraphs and line breaks](#3-paragraphs-and-line-breaks)
- [4. Lists](#4-lists)
  - [Unordered list](#unordered-list)
  - [Ordered list](#ordered-list)
  - [Nested or multilevel list](#nested-or-multilevel-list)
- [5. Links](#5-links)
  - [Internal links](#internal-links)
- [6. Images](#6-images)
- [7. Code](#7-code)
  - [Code within a sentence](#code-within-a-sentence)
  - [Code blocks](#code-blocks)
- [8. Blockquotes](#8-blockquotes)
- [9. Tables](#9-tables)
- [10. Horizontal rules](#10-horizontal-rules)
- [11. Hidden comments](#11-hidden-comments)
- [12. Visual Studio Code](#12-visual-studio-code)
  - [Preview](#preview)
  - [Generate an automatic table of contents](#generate-an-automatic-table-of-contents)
    - [Installation](#installation)
    - [Creating the table of contents](#creating-the-table-of-contents)
- [13. References](#13-references)
 

## 1. Headings and sections

In Markdown, the `#` symbol is used to create headings:

```
# Main heading
## Section
### Subsection
#### Subsection level
##### Lower level
```

The ***space after `#`*** is important.

---

## 2. Text formatting

### Bold

```markdown
**Bold text**
```

### Italic

```markdown
*Italic text*
```

### Bold and italic

```markdown
***Bold and italic***
```


## 3. Paragraphs and line breaks

To create a new paragraph, leave an empty line.

```markdown
First paragraph.

Second paragraph.
```

To force a line break, add two spaces at the end of the line.

---


## 4. Lists

### Unordered list

```markdown
- Item 1
- Item 2
- Item 3
```

Again, the space after `-` is important.

### Ordered list

```markdown
1. Item 1
2. Item 2
3. Item 3
```

### Nested or multilevel list

```markdown
- Main item 1
  - Subitem 1
  - Subitem 2
- Main item 2
```

---

## 5. Links

The structure of a link is:

```markdown
[Visible text](https://example.com)
```

A web address can also be displayed directly:

```markdown
<https://example.com>
```

### Internal links

Internal links are used to link to a section within the same document:

```markdown
[Go to the lists section](#4-lists)
```

Normally, to turn a heading into an identifier, it is written in lowercase, spaces are replaced with hyphens, and punctuation marks are removed.

## 6. Images

For local use, the images must first be downloaded. It is recommended to store them in a separate folder. To insert an image:

```markdown
![Image description](images/example.png)
```

An image hosted on the internet can also be used:

```markdown
![Description](https://example.com/image.png)
```

## 7. Code

### Code within a sentence

When a word or instruction is mentioned as code within a paragraph, it is written between backticks:

```text
`code that is not executed`
```

Example:

```markdown
The `print()` function displays information.
```

Inline code is not executed. It is simply displayed with a different visual format to distinguish it from the rest of the text.

A backslash indicates that the following character must be displayed literally:

```markdown
\# This appears as normal text
```


### Code blocks

When the code occupies several lines, a code block is used.

The block begins and ends with three backticks:

````text
```
First line
Second line
Third line
```
````

In the preview, it will appear inside a box.

## 8. Blockquotes

Blockquotes make it possible to highlight a passage and visually separate it from the main content.

They are created by placing the `>` symbol at the beginning of the line.

```markdown
> First line of the blockquote.
> Second line of the blockquote.
> Third line of the blockquote.
```

A blockquote can also be placed inside another blockquote by using several `>` symbols:

```markdown
> Main blockquote.
>
>> Blockquote inside the main blockquote.
```

## 9. Tables

A basic table is written as follows:

```markdown
| Column 1 | Column 2 | Column 3 |
|---|---|---|
| Data 1 | Data 2 | Data 3 |
| Data 4 | Data 5 | Data 6 |
```

- `:---` aligns the content to the left.
- `:---:` centers the content.
- `---:` aligns the content to the right.

```markdown
| Left | Center | Right |
|:---|:---:|---:|
| Text | Text | Text |
| Text | Text | Text |
```

## 10. Horizontal rules

A horizontal rule visually separates two parts of a document. It is recommended to leave an empty line before and after it.

```markdown
---
```

## 11. Hidden comments

```markdown
<!--
This is an internal comment.

It can span several lines.
-->
```

Although comments do not appear in the preview, they are visible when the original file or the source code is opened on GitHub. They should not contain private information.

## 12. Visual Studio Code

### Preview

To open the preview:

```text
Ctrl + Shift + V
```

To open the editor and preview at the same time:

```text
Ctrl + K
```

and then:

```text
V
```

### Generate an automatic table of contents


To insert a table of contents that forms part of the file itself, the **Markdown All in One** extension can be used.

#### Installation

1. Open the **Extensions** section in Visual Studio Code.
2. Search for `Markdown All in One`.
3. Check that the extension is published by **Yu Zhang**.
4. Select **Install**.


#### Creating the table of contents

1. Place the cursor where the table of contents should be inserted.
2. Open the command palette using the shortcut:

```text
Ctrl + Shift + P
```

3. Search for and run:

```text
Markdown All in One: Create Table of Contents
```

The extension will analyze the headings and generate a list of internal links. To update the table of contents, simply save the document:

```text
Ctrl + S
```

Sometimes, a heading should be displayed in the document without being included in the automatic table of contents.

To exclude it, add the `<!-- omit from toc -->` comment at the end of the heading:

```text
# Document heading <!-- omit from toc -->
```

## 13. References

The following sources were consulted to verify the syntax and features described in this guide:

1. CommonMark. [CommonMark Specification](https://spec.commonmark.org/current/).  
   Reference specification for basic Markdown syntax.

2. GitHub Docs. [Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).  
   Documentation on the use of Markdown and GitHub Flavored Markdown on GitHub.

3. Microsoft. [Markdown and Visual Studio Code](https://code.visualstudio.com/docs/languages/markdown).  
   Official documentation on editing, previewing, and navigating Markdown files in Visual Studio Code.

4. Zhang, Yu. [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one).  
   Visual Studio Code extension used to generate and automatically update the table of contents.



<!--
Pending:

Create a README page that provides options to open the guide in Spanish or English.

-->