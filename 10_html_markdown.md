# Chapter 10 — HTML in Markdown

Markdown is intentionally simple.

That simplicity makes it easy to learn and write, but it also means some features are missing.

For example, standard Markdown cannot:

- Resize images
- Center text
- Change image alignment
- Create collapsible sections
- Use custom colors
- Embed videos
- Create advanced layouts

Fortunately, GitHub allows a subset of HTML inside Markdown documents.

This gives you the flexibility of HTML while keeping the readability of Markdown.

By the end of this chapter, you'll learn:

- Why HTML is supported
- When to use HTML
- Text alignment
- Image resizing
- Image alignment
- Line breaks
- Collapsible sections
- HTML comments
- Embedded videos
- Best practices
- Common mistakes

---

# Why Use HTML?

Markdown covers most documentation needs.

However, some layouts simply aren't possible with pure Markdown.

Instead of replacing Markdown entirely, GitHub allows many HTML elements inside Markdown files.

Think of HTML as a toolbox for the features Markdown doesn't provide.

---

# When Should You Use HTML?

Use HTML when Markdown cannot achieve the desired result.

Good examples include:

- Resizing images
- Centering content
- Creating collapsible sections
- Adding custom tables
- Embedding videos
- Creating complex layouts

Whenever Markdown can accomplish the same task, prefer Markdown.

---

# Text Alignment

Markdown doesn't support text alignment.

HTML does.

## Center Alignment

```html
<p align="center">
This text is centered.
</p>
```

Output

<p align="center">
This text is centered.
</p>

---

## Right Alignment

```html
<p align="right">
This text is right aligned.
</p>
```

Output

<p align="right">
This text is right aligned.
</p>

---

# Line Breaks

Markdown usually ignores single line breaks.

HTML provides the `<br>` element.

Example

```html
Hello<br>
World
```

Output

Hello<br>
World

---

# Horizontal Lines

HTML also provides horizontal rules.

```html
<hr>
```

Markdown already supports:

```md
---
```

Prefer Markdown unless HTML is required.

---

# Image Resizing

Markdown cannot resize images.

HTML can.

```html
<img src="assets/logo.png" width="300">
```

You can also specify height.

```html
<img src="assets/logo.png" width="300" height="200">
```

---

# Image Alignment

Center an image.

```html
<p align="center">
    <img src="assets/logo.png" width="250">
</p>
```

Right alignment.

```html
<p align="right">
    <img src="assets/logo.png" width="250">
</p>
```

---

# Image Captions

Markdown doesn't have captions.

One simple approach is:

```html
<p align="center">
    <img src="assets/dashboard.png" width="600">
</p>

<p align="center">
<i>Figure 1: Dashboard</i>
</p>
```

---

# Collapsible Sections

One of the most useful HTML features.

GitHub supports the `<details>` element.

Example

```html
<details>

<summary>Click to Expand</summary>

Hidden content appears here.

</details>
```

Output

<details>

<summary>Click to Expand</summary>

Hidden content appears here.

</details>

---

# FAQ Example

```html
<details>

<summary>How do I install this project?</summary>

Run:

```bash
pip install -r requirements.txt
```

</details>
```

Perfect for long FAQs.

---

# HTML Comments

Sometimes you want to leave notes inside your Markdown source.

HTML comments won't appear in the rendered document.

```html
<!-- TODO: Update screenshot -->
```

Readers never see them.

---

# Embedded Videos

GitHub doesn't allow embedded YouTube videos using `<iframe>`.

Instead, use an image linked to the video.

```md
[![Watch Demo](assets/demo-thumbnail.png)](https://youtube.com)
```

This is the recommended approach.

---

# HTML Tables

HTML tables support features unavailable in Markdown.

Example

```html
<table>
<tr>
<td>Python</td>
<td>Easy</td>
</tr>
</table>
```

Use HTML tables only when Markdown tables are insufficient.

---

# Mixing Markdown and HTML

GitHub allows both together.

Example

```md
# Bella Voice Assistant

<p align="center">
<img src="assets/logo.png" width="200">
</p>

## Features

- AI Chat
- News Reader
- Voice Commands
```

This is extremely common in professional repositories.

---

# Supported HTML Tags

GitHub supports many safe HTML elements.

Some commonly used ones include:

| Tag | Purpose |
|------|---------|
| `<p>` | Paragraph |
| `<img>` | Images |
| `<br>` | Line break |
| `<details>` | Collapsible content |
| `<summary>` | Collapsible title |
| `<table>` | Tables |
| `<tr>` | Table row |
| `<td>` | Table cell |
| `<strong>` | Bold text |
| `<em>` | Italic text |
| `<sub>` | Subscript |
| `<sup>` | Superscript |

Some HTML elements are intentionally blocked for security reasons.

---

# Best Practices

✔ Use Markdown whenever possible.

✔ Use HTML only when necessary.

✔ Keep HTML simple.

✔ Test your README on GitHub.

✔ Prefer `<details>` instead of huge sections.

✔ Resize large images.

---

# Common Mistakes

## Writing Entire Documents in HTML

❌

Everything is HTML.

Markdown becomes unreadable.

Instead:

Use Markdown first.

---

## Overusing Center Alignment

Center only important elements like:

- Project logo
- Badges
- Banner

Don't center entire documents.

---

## Huge Images

Always resize screenshots.

Large images make READMEs difficult to read.

---

## Using Unsupported HTML

GitHub sanitizes HTML.

Some tags, attributes, and scripts are removed for security.

Always preview your README after publishing.

---

# Real Project Example

Imagine your Bella repository.

```md
# Bella Voice Assistant

<p align="center">
<img src="assets/logo.png" width="180">
</p>

<p align="center">
A Python-powered AI Voice Assistant
</p>

## Installation

> [!IMPORTANT]
> Python 3.13 is required.

<details>

<summary>View Installation Steps</summary>

```bash
git clone https://github.com/user/bella.git

cd bella

pip install -r requirements.txt
```

</details>
```

Notice how Markdown and HTML complement each other.

---

# Compatibility

| Feature | GitHub |
|----------|:------:|
| `<details>` | ✅ |
| `<img>` | ✅ |
| `<br>` | ✅ |
| `<table>` | ✅ |
| `<iframe>` | ❌ |
| `<script>` | ❌ |

---

# Did You Know?

GitHub sanitizes HTML before rendering it.

This prevents malicious scripts from running inside README files and helps keep repositories safe.

---

# Pro Tip

If you're unsure whether to use Markdown or HTML, ask yourself:

> "Can Markdown do this?"

If the answer is **yes**, use Markdown.

If the answer is **no**, HTML is usually the right choice.

---

# Mini Exercise

Create a README section that contains:

- A centered project logo
- A collapsible FAQ
- A resized image
- A hidden HTML comment

Try it before viewing the solution.

<details>

<summary>Solution</summary>

````md
<!-- Update logo before release -->

<p align="center">
<img src="assets/logo.png" width="180">
</p>

<details>

<summary>How do I install the project?</summary>

```bash
pip install -r requirements.txt
```

</details>
