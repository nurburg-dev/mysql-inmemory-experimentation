---
title: This is a sample project
video: https://www.youtube.com/watch?v=7ySVWcFHz98
tags:
  - mysql
  - redis
  - golang
summary: This is the summary of a sample project
---

I had no knowledge of frontmatter until I started learning Astro. Here are some notes on what it is, some syntax tips, and notes on YAML in general.

> I can't find why you would use them in Markdown files, except for blog posts in Astro. Would a keyword-rich `description` enable your repo to be found more often on searches?

## What exactly is Frontmatter

[What exactly is Frontmatter](https://daily-dev-tips.com/posts/what-exactly-is-frontmatter/)

Frontmatter is a way to identify metadata in Markdown files. Metadata can literally be anything you want it to be, but often it's used for data elements your page needs and you don't want to show directly.

Some examples of common metadata are (the table above the H1 at the top of this file is the frontmatter for the page):

- Title of the post
- Description for SEO purposes
- Tags that belong to a document
- The date it was written
- The author(s)

To add Frontmatter to a Markdown document, you have to start by writing a three-dotted block at the top of your file:

```markdown
---
title: Frontmatter section
---
```

Everything in there will be seen as metadata, and that block **_MUST_** be the first thing in your file!

## Basic Frontmatter options

It's important to note that **Frontmatter is parsed as `YAML` blocks**, so the indentation is important

- Set regular variables with a colon setup
- Or convert them into an array of objects
- You can even use the bracket way of defining arrays
- You can have multidimensional object arrays
- You can use multi-line text blocks using the pipe method

> NOTE: the indentation displayed in the code block below is "off". See the source code for the actual indentation used.

## Bridgetown Front Matter

[Front Matter](https://www.bridgetownrb.com/docs/front-matter)

Front matter is a snippet of YAML or Ruby data which sits at the top of a file between special line delimiters. You can think of front matter as a datastore consisting of one or more key-value pairs.

Any file that contains a front matter block will be specially processed by Bridgetown.

> What or who is _Bridgetown_?

The front matter must be the first thing in the file and must either take the form of valid YAML set between triple-dashed lines, or one of several Ruby-based formats.

Between these triple-dashed lines, you can set predefined variables or add custom variables of your own.

## what-is-frontmatter.md

[what-is-frontmatter.md](https://github.com/cuttlebelle/website/blob/master/content/documentation/what-is-frontmatter.md)

With front-matter we can add more complex data to our content than just blobs of text. Front-matter has to be on the top of the file and begins and ends with three dashes `---`.

## Dendron: Frontmatter

Frontmatter is a collection of custom attributes at the top of each Markdown file. The beginning and end of this is indicated by `---`.

Frontmatter is YAML that you can add to the front of your Markdown file. It was first introduced by Jekyll and is a convenient way of adding metadata to your plaintext documents.

## YAML Tutorial

[YAML Tutorial : A Complete Language Guide with Examples](https://spacelift.io/blog/yaml)

A YAML format primarily uses 3 node types:

1. Maps/Dictionaries (YAML calls it mapping):
   The content of a mapping node is an unordered set of key/value node pairs, with the restriction that each of the keys is unique. YAML places no further restrictions on the nodes.
1. Arrays/Lists (YAML calls them sequences):
   The content of a sequence node is an ordered series of zero or more nodes. In particular, a sequence may contain the same node more than once. It could even contain itself.
1. Literals (Strings, numbers, boolean, etc.):
   The content of a scalar node is an opaque datum that can be presented as a series of zero or more Unicode characters.

### Indentation

A YAML file relies on whitespace and indentation to indicate nesting.

It is critical to note that tab characters cannot be used for indentation in YAML files; only spaces can be used. The number of spaces used for indentation doesn’t matter as long as they are consistent.

### Mapping

Mappings are used to associate key/value pairs that are unordered. Maps can be nested by increasing the indentation, or new maps can be created at the same level by resolving the previous one.

### Sequences

Sequences in YAML are represented by using the hyphen (`-`) and space. They are ordered and can be embedded inside a map using indentation.

Tip: Remember that the order matters with sequences but not with mappings.

### Literals — Strings

The string literals do not require to be quoted. It is only important to quote them when they contain a value that can be mistaken as a special character

1. Folding Strings: Strings can also be written in blocks and be interpreted without the new line characters using the fold operator (greater than `>`).
1. Block strings: Strings can be interpreted as blocks using the block (pipe `|`) character. This is interpreted with the new lines (`\n`)
1. Chomp characters: Multiline strings may end with whitespaces. Preserve chomp(`+`) and strip chomp operators can be used either to preserve or strip the whitespaces. They can be used with block and pipe characters. tripping new line character (`-`)

## Comments

YAML file also supports comments, unlike JSON. A comment starts with `#`.
