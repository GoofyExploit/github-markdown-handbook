# Chapter 2 — Headings

Headings are one of the most important features in Markdown.

They organize your document into sections, making it easier for readers to navigate and understand your content.

Whether you're writing a simple README or a large technical handbook, headings provide structure and improve readability.

By the end of this chapter, you'll learn:

- What headings are
- How to create headings
- The six heading levels
- Best practices for using headings
- Internal links
- Common mistakes
- Real-world examples

---

# What is a Heading?

A heading is a title for a section of your document.

Think of headings like chapters in a book.

For example:

```
Book

Chapter 1
    Topic A
    Topic B

Chapter 2
    Topic C
```

Markdown works the same way.

A well-structured document allows readers to quickly find the information they're looking for.

---

# Creating Headings

Markdown uses the **hash (`#`) symbol** to create headings.

The number of `#` symbols determines the heading level.

```md
# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6
```

Output:

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

---

# Understanding Heading Levels

Markdown supports **six heading levels**.

| Markdown | Level | Typical Use |
|-----------|-------|-------------|
| `#` | Heading 1 | Document title |
| `##` | Heading 2 | Major section |
| `###` | Heading 3 | Subsection |
| `####` | Heading 4 | Small subsection |
| `#####` | Heading 5 | Rarely used |
| `######` | Heading 6 | Very rarely used |

---

# Which Heading Should You Use?

A good document follows a logical hierarchy.

Example:

```text
# GitHub Markdown Handbook

## Introduction

## Installation

### Windows

### Linux

## Usage

### Basic Usage

### Advanced Usage

## License
```

Notice how each level is nested inside the one above it.

---

# Heading Hierarchy

Avoid skipping heading levels.

✅ Good

```md
# Project

## Installation

### Linux
```

❌ Bad

```md
# Project

#### Linux
```

Jumping directly from `#` to `####` makes your document difficult to follow.

---

# One H1 Rule

Most Markdown documents should contain **only one H1 (`#`) heading**.

That H1 is usually the title of your document.

Example:

```md
# Bella AI Assistant
```

Everything else should begin with `##`.

Good example:

```md
# Bella

## Features

## Installation

## Usage

## License
```

---

# Headings in README Files

A professional README usually follows this structure:

```md
# Project Name

## Features

## Installation

## Usage

## Screenshots

## Roadmap

## Contributing

## License
```

Readers immediately know where to find information.

---

# Internal Links

GitHub automatically creates anchor links for headings.

Example:

```md
## Installation
```

can be linked like this:

```md
[Go to Installation](#installation)
```

Another example:

```md
## Project Structure
```

becomes

```md
[Project Structure](#project-structure)
```

---

# How GitHub Generates Anchor Links

GitHub automatically converts headings into lowercase.

Spaces become hyphens.

For example:

```md
## My First Project
```

becomes

```text
#my-first-project
```

Examples:

| Heading | Anchor |
|----------|---------|
| Installation | `#installation` |
| Project Structure | `#project-structure` |
| Frequently Asked Questions | `#frequently-asked-questions` |

---

# Table of Contents

Internal links make it possible to create a Table of Contents.

Example:

```md
# Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)
```

This is especially useful for long README files.

---

# Best Practices

✔ Use only one H1.

✔ Keep heading names short.

✔ Use clear and descriptive titles.

✔ Follow a logical hierarchy.

✔ Use title case consistently.

Example:

```text
Installation

Usage

License
```

instead of

```text
installation

USAGE

license
```

---

# Common Mistakes

## Using Too Many H1 Headings

❌

```md
# Features

# Installation

# Usage
```

✅

```md
# Project Name

## Features

## Installation

## Usage
```

---

## Skipping Heading Levels

❌

```md
# Project

#### Installation
```

✅

```md
# Project

## Installation
```

---

## Long Heading Names

❌

```text
How to Install This Amazing Project on Windows Operating Systems
```

✅

```text
Windows Installation
```

---

# Real Project Example

Imagine you're documenting a weather application.

```md
# Weather App

## Features

## Installation

### Windows

### Linux

## Configuration

## Usage

## API

## Screenshots

## Roadmap

## License
```

This structure is easy to understand and scales well as the project grows.

---

# Mini Exercise

Create the heading structure for a project called **Task Manager**.

It should include:

- Features
- Installation
- Usage
- Screenshots
- License

Try writing it yourself before checking the solution.

<details>

<summary>Solution</summary>

```md
# Task Manager

## Features

## Installation

## Usage

## Screenshots

## License
```

</details>

---

# Summary

In this chapter, you learned:

- What headings are
- The six heading levels
- How heading hierarchy works
- Why most documents should have only one H1
- How GitHub generates anchor links
- How to build a Table of Contents
- Best practices for organizing documentation

Headings are the foundation of every well-written Markdown document.

---

# Next Chapter

➡ **Chapter 3 — Text Formatting**

In the next chapter, you'll learn how to make text **bold**, *italic*, ~~strikethrough~~, use `inline code`, and format content for better readability.
