# Chapter 5 — Code Blocks & Syntax Highlighting

Code is at the heart of technical documentation.

Whether you're writing installation instructions, sharing configuration files, or demonstrating examples, properly formatted code blocks make your documentation easier to read and understand.

GitHub Markdown supports both **inline code** and **fenced code blocks** with syntax highlighting for hundreds of programming languages.

By the end of this chapter, you'll learn:

- Inline code
- Fenced code blocks
- Syntax highlighting
- Supported languages
- Showing raw Markdown
- Diff code blocks
- Plain text blocks
- Best practices
- Common mistakes

---

# Why Code Blocks Matter

Imagine reading installation instructions like this:

Clone the repository using git clone, install the dependencies using pip install -r requirements.txt, and then run python main.py.

Now compare it with this:

```bash
git clone https://github.com/username/project.git
cd project
pip install -r requirements.txt
python main.py
```

The second example is much easier to read and copy.

---

# Inline Code

Inline code is used for short pieces of code within a sentence.

## Syntax

```md
Use `pip install` to install packages.
```

Output:

Use `pip install` to install packages.

---

## When Should You Use Inline Code?

Use inline code for:

- Commands
- File names
- Variables
- Function names
- Class names
- Package names
- Environment variables

Examples:

```md
Run `python main.py`.

Edit `config.py`.

Set the `PORT` variable.

Call the `main()` function.
```

---

# Fenced Code Blocks

For multiple lines of code, use fenced code blocks.

A fenced code block starts and ends with three backticks.

## Syntax

````md
```
Hello World
```
