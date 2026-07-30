# Chapter 3 — Text Formatting

Text formatting helps emphasize important information, improve readability, and make your documentation more engaging.

Markdown provides several simple ways to style text without writing HTML.

By the end of this chapter, you'll learn:

- Bold text
- Italic text
- Bold + Italic
- Strikethrough
- Inline code
- Escaping Markdown characters
- Horizontal rules
- Line breaks
- Best practices
- Common mistakes

---

# Why Text Formatting Matters

Imagine reading a page where every sentence looks exactly the same.

It quickly becomes difficult to identify:

- Important information
- Commands
- File names
- Warnings
- Notes

Formatting allows readers to scan your documentation quickly and find what they need.

Good formatting improves readability without making the document feel cluttered.

---

# Bold Text

Bold text is used to emphasize important words or phrases.

## Syntax

```md
**Bold Text**
```

or

```md
__Bold Text__
```

Output

**Bold Text**

---

## When Should You Use Bold?

Use bold for:

- Important notes
- Keywords
- Section highlights
- Critical instructions

Example

```md
Install **Python 3.13** before running this project.
```

Output

Install **Python 3.13** before running this project.

---

# Italic Text

Italic text is used for subtle emphasis.

## Syntax

```md
*Italic Text*
```

or

```md
_Italic Text_
```

Output

*Italic Text*

---

## When Should You Use Italics?

Italics work well for

- Introducing new terms
- Book titles
- Gentle emphasis
- Notes

Example

```md
*Markdown* is easy to learn.
```

Output

*Markdown* is easy to learn.

---

# Bold + Italic

You can combine both styles.

## Syntax

```md
***Very Important***
```

Output

***Very Important***

---

Use this sparingly.

If everything is emphasized, nothing stands out.

---

# Strikethrough

Strikethrough indicates deleted, removed, or outdated content.

## Syntax

```md
~~Deprecated~~
```

Output

~~Deprecated~~

---

Example

```md
Python 3.7 ~~Recommended~~

Python 3.13 Recommended
```

Output

Python 3.7 ~~Recommended~~

Python 3.13 Recommended

---

# Inline Code

Inline code is one of the most important formatting features.

Use it whenever mentioning

- Commands
- Variables
- File names
- Function names
- Programming keywords

## Syntax

```md
Use `pip install` to install packages.
```

Output

Use `pip install` to install packages.

---

More examples

```md
`main.py`

`README.md`

`requirements.txt`

`git clone`

`python main.py`
```

---

# Multiple Inline Code Examples

Markdown allows multiple inline code blocks.

```md
Run `git clone` and then execute `python main.py`.
```

Output

Run `git clone` and then execute `python main.py`.

---

# Escaping Markdown Characters

Sometimes you want Markdown symbols to appear as plain text.

Use a backslash (`\`).

## Example

```md
\*

\#

\`

\_
```

Output

\*

\#

\`

\_

---

# Horizontal Rules

Horizontal rules divide large sections of your document.

## Syntax

```md
---
```

or

```md
***
```

or

```md
___
```

Output

---

Horizontal rules improve readability by separating unrelated sections.

---

# Line Breaks

Markdown ignores multiple blank spaces.

Example

```md
Hello
World
```

may render as

Hello World

To force a new line, use one of these methods.

### Method 1

Leave a blank line.

```md
Hello

World
```

Output

Hello

World

---

### Method 2

Use HTML

```html
Hello<br>
World
```

Output

Hello  
World

---

# Combining Formatting

Markdown formatting can be combined.

Example

```md
This is **bold**, *italic*, and `inline code`.
```

Output

This is **bold**, *italic*, and `inline code`.

---

Another example

```md
The command `pip install` must be run before starting the application.
```

Output

The command `pip install` must be run before starting the application.

---

# Formatting File Names

Always place file names inside inline code.

Good

```md
Edit `config.py`.
```

Bad

```md
Edit config.py.
```

---

# Formatting Commands

Commands should always be written using inline code.

Good

```md
Run `git status`.
```

Bad

```md
Run git status.
```

---

# Formatting Variables

Variables should also use inline code.

Example

```md
Set the `PORT` environment variable.
```

---

# Best Practices

✔ Use bold for important information.

✔ Use italics for gentle emphasis.

✔ Use inline code for commands.

✔ Use inline code for file names.

✔ Don't overuse bold.

✔ Don't overuse italics.

✔ Keep formatting consistent.

---

# Common Mistakes

## Too Much Bold

❌

```md
**This project is very useful and every command is important.**
```

Everything becomes difficult to read.

---

## Using Italics for Commands

❌

```md
*git clone*
```

Commands should use inline code.

✅

```md
`git clone`
```

---

## Forgetting Inline Code

❌

Install pip install requests

✅

Install `pip install requests`

---

## Mixing Styles Randomly

❌

```md
**Installation**

*Requirements*

`Usage`

```

Instead, use formatting consistently.

---

# Real Project Example

Imagine you're documenting a Python application.

```md
# Weather App

Install the required packages using `pip install -r requirements.txt`.

Run the application with `python main.py`.

This project requires **Python 3.13**.

*Windows and Linux are supported.*

~~Python 3.8~~

Python 3.13
```

Notice how formatting makes the documentation easier to scan.

---

# Mini Exercise

Write a sentence that contains

- one bold phrase
- one italic phrase
- one inline command
- one file name

Try writing it before viewing the solution.

<details>

<summary>Solution</summary>

```md
Install **Python 3.13**, then run `python main.py`.

Configuration is stored inside `config.py`.

*Linux users* should install dependencies first.
```

</details>

---

# Summary

In this chapter, you learned

- Bold text
- Italic text
- Bold + Italic
- Strikethrough
- Inline code
- Escaping characters
- Horizontal rules
- Line breaks
- Best practices
- Common mistakes

These formatting techniques will make your documentation cleaner, more readable, and more professional.

---

# Key Takeaways

- Use **bold** for emphasis.
- Use *italics* sparingly.
- Use `inline code` for commands, files, variables, and keywords.
- Keep formatting consistent.
- Don't over-format your documentation.

---

# Next Chapter

➡ **Chapter 4 — Lists**

In the next chapter, you'll learn how to create bulleted lists, numbered lists, nested lists, task lists, and organize information effectively.
