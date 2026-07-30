# Chapter 9 — Blockquotes & GitHub Alerts

Not every piece of information in your documentation has the same level of importance.

Sometimes you want to:

- Highlight a warning
- Add an important note
- Display a tip
- Quote someone
- Separate additional information from the main content

Markdown provides **blockquotes**, while GitHub Flavored Markdown (GFM) extends them with beautiful **Alerts**.

By the end of this chapter, you'll learn:

- Blockquotes
- Nested blockquotes
- Multi-line blockquotes
- Blockquotes with formatting
- GitHub Alerts
- Available alert types
- Best practices
- Common mistakes

---

# Why Use Blockquotes?

Imagine reading this sentence in the middle of a README:

Delete the configuration file before running the application.

It doesn't stand out.

Now compare it with:

> **Warning**
>
> Delete the configuration file before running the application.

The important information immediately catches the reader's attention.

---

# Creating a Blockquote

A blockquote begins with the `>` character.

Syntax

```md
> This is a blockquote.
```

Output

> This is a blockquote.

---

# Multi-Line Blockquotes

Every quoted line begins with `>`.

Example

```md
> Markdown is simple.
>
> It allows you to write clean documentation
> without using HTML.
```

Output

> Markdown is simple.
>
> It allows you to write clean documentation
> without using HTML.

---

# Multiple Paragraphs

Blank lines are also prefixed with `>`.

Example

```md
> Paragraph One.
>
> Paragraph Two.
```

Output

> Paragraph One.
>
> Paragraph Two.

---

# Nested Blockquotes

Blockquotes can be nested.

Example

```md
> Main Quote
>
>> Nested Quote
>>
>>> Third Level
```

Output

> Main Quote
>
>> Nested Quote
>>
>>> Third Level

Nested blockquotes are rarely needed but are fully supported.

---

# Formatting Inside Blockquotes

Markdown formatting works inside blockquotes.

Example

```md
> **Important**
>
> Install `Python 3.13` before running the project.
```

Output

> **Important**
>
> Install `Python 3.13` before running the project.

---

# Lists Inside Blockquotes

Lists work normally.

Example

```md
> Requirements
>
> - Python
> - Git
> - VS Code
```

Output

> Requirements
>
> - Python
> - Git
> - VS Code

---

# Code Blocks Inside Blockquotes

You can include fenced code blocks.

````md
> Example
>
> ```bash
> python main.py
> ```
