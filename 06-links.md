# Chapter 6 — Links

Links are one of the most powerful features in Markdown.

They allow you to connect your documentation with websites, files, images, email addresses, and even other sections within the same document.

A well-organized README uses links to help readers quickly find the information they need.

By the end of this chapter, you'll learn:

- Inline links
- Automatic links
- Email links
- Relative links
- Anchor links
- Image links
- Reference-style links
- Best practices
- Common mistakes

---

# Why Links Matter

Imagine a README that says:

> Visit our website.

Which website?

Now compare it with:

> Visit our [official website](https://example.com).

Readers can immediately access the resource.

Links improve navigation and make your documentation much more useful.

---

# Creating a Link

The basic syntax is:

```md
[Link Text](https://example.com)
```

Example

```md
[GitHub](https://github.com)
```

Output

[GitHub](https://github.com)

---

# Understanding the Syntax

A Markdown link has two parts.

```md
[Visible Text](Destination)
```

Example

```md
[Python](https://python.org)
```

- `[]` contains the text users see.
- `()` contains the destination.

---

# Linking to Websites

Examples

```md
[Python](https://python.org)

[GitHub](https://github.com)

[OpenAI](https://openai.com)
```

Output

- [Python](https://python.org)
- [GitHub](https://github.com)
- [OpenAI](https://openai.com)

---

# Automatic Links

GitHub automatically detects URLs.

Example

```md
https://github.com
```

Output

https://github.com

Although this works, using descriptive text is usually better.

Instead of

```md
https://github.com/user/project
```

write

```md
[Project Repository](https://github.com/user/project)
```

---

# Email Links

You can create clickable email addresses.

Syntax

```md
<example@email.com>
```

Output

<example@email.com>

You can also use

```md
[Contact Us](mailto:example@email.com)
```

---

# Relative Links

Relative links connect files within the same repository.

Suppose your project looks like this:

```text
project/

README.md

LICENSE

docs/

installation.md

assets/

logo.png
```

From `README.md`, you can link to another file like this:

```md
[Installation Guide](docs/installation.md)
```

This works even if someone forks or clones your repository.

---

# Linking to Parent Directories

Suppose you're inside:

```text
docs/

guide.md
```

and want to link back to the README.

```md
[Home](../README.md)
```

`..` means "go up one directory."

---

# Anchor Links

GitHub automatically creates anchors for headings.

Example

```md
## Installation
```

can be linked using

```md
[Go to Installation](#installation)
```

For multi-word headings

```md
## Project Structure
```

becomes

```md
[Project Structure](#project-structure)
```

---

# Table of Contents

Anchor links are commonly used to create a table of contents.

Example

```md
## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)
```

Readers can jump directly to each section.

---

# Linking Images

Images themselves can also act as links.

Syntax

```md
[![Logo](assets/logo.png)](https://github.com)
```

Clicking the image opens the destination.

This is commonly used for badges and logos.

---

# Reference-Style Links

When using the same link multiple times, reference-style links keep your document cleaner.

Example

```md
Visit the [Python Website][python].

[python]: https://python.org
```

Output

Visit the [Python Website][python].

[python]: https://python.org

This is useful for long documents with many repeated links.

---

# Linking to Downloads

You can link directly to downloadable files.

Example

```md
[Download PDF](docs/guide.pdf)
```

---

# Combining Links with Formatting

Links work with other Markdown formatting.

Example

```md
**[GitHub Repository](https://github.com)**
```

or

```md
*Visit the [Documentation](docs/index.md).*
```

---

# Best Practices

✔ Use descriptive link text.

✔ Prefer relative links for repository files.

✔ Test every link before publishing.

✔ Keep link names short and meaningful.

✔ Use HTTPS whenever possible.

---

# Common Mistakes

## Using "Click Here"

❌

```md
[Click Here](https://example.com)
```

Better

```md
[Installation Guide](docs/install.md)
```

Readers should know where the link goes before clicking.

---

## Broken Relative Paths

❌

```md
[Guide](guide.md)
```

If the file is actually inside `docs/`, the link won't work.

Correct

```md
[Guide](docs/guide.md)
```

---

## Using Absolute GitHub URLs

Instead of

```md
https://github.com/user/project/blob/main/docs/install.md
```

prefer

```md
[Installation](docs/install.md)
```

Relative links continue working even if the repository is renamed or forked.

---

# Real Project Example

Imagine your repository contains:

```text
Bella/

README.md

LICENSE

docs/

installation.md

configuration.md

assets/

logo.png
```

Your README could contain:

```md
## Documentation

- [Installation Guide](docs/installation.md)
- [Configuration](docs/configuration.md)

## Resources

- [Python](https://python.org)
- [OpenAI](https://platform.openai.com)

## Contact

<support@example.com>
```

Everything is neatly connected.

---

# Did You Know?

GitHub automatically checks many internal repository links.

If a linked file doesn't exist, users will receive a **404 page** when they click it.

Testing links before publishing is always a good idea.

---

# Pro Tip

Avoid displaying long URLs directly.

Instead of

```text
https://github.com/username/project/blob/main/docs/getting-started.md
```

write

```md
[Getting Started Guide](docs/getting-started.md)
```

Your documentation will look much cleaner.

---

# Mini Exercise

Create a section containing:

- A website link
- A relative link
- An email link
- A table of contents with two anchor links

Try it yourself before viewing the solution.

<details>

<summary>Solution</summary>

```md
## Table of Contents

- [Installation](#installation)
- [Usage](#usage)

## Resources

- [GitHub](https://github.com)
- [Installation Guide](docs/installation.md)

## Contact

<support@example.com>
```

</details>

---

# Quick Quiz

### 1. Which syntax creates a hyperlink?

A. `{Google}(https://google.com)`

B. `[Google](https://google.com)`

C. `(Google)[https://google.com]`

**Answer:** **B**

---

### 2. Which type of link should you use for another file inside the same repository?

**Answer:** Relative link.

---

### 3. What is the anchor for this heading?

```md
## Getting Started
```

A. `#Getting Started`

B. `#getting-started`

C. `#getting_started`

**Answer:** **B**

---

# Summary

In this chapter, you learned:

- Inline links
- Automatic links
- Email links
- Relative links
- Anchor links
- Reference-style links
- Image links
- Best practices
- Common mistakes

Links transform a collection of documents into a connected and easy-to-navigate project.

---

# Key Takeaways

- Use descriptive link text.
- Prefer relative links for repository files.
- Use anchor links for long documents.
- Test every link before publishing.
- Avoid long raw URLs when descriptive text works better.

---

# Next Chapter

➡ **Chapter 7 — Images**

In the next chapter, you'll learn how to add images, GIFs, screenshots, logos, resize images with HTML, align images, create clickable images, and organize visual content to make your README stand out.
