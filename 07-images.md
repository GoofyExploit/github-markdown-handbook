# Chapter 7 — Images

A picture is often worth more than a paragraph of text.

Whether you're showcasing your application, explaining a workflow, or displaying a project logo, images make your documentation more engaging and easier to understand.

GitHub Markdown allows you to add images with just a few characters, while HTML gives you additional control over size and alignment.

By the end of this chapter, you'll learn:

- Adding images
- Image paths
- Alternative text
- Local vs Remote images
- Clickable images
- GIFs
- Image resizing
- Image alignment
- Best practices
- Common mistakes

---

# Why Images Matter

Imagine opening a project repository.

README A:

- Features
- Installation
- Usage

README B:

- Features
- Screenshots
- Demo GIF
- Logo
- Installation

Which one looks more professional?

Images immediately give readers confidence about what the project looks like.

They also make documentation much easier to follow.

---

# Adding an Image

The basic syntax is:

```md
![Alternative Text](image-path)
```

Example:

```md
![GitHub Logo](assets/github-logo.png)
```

If the image exists, GitHub displays it.

---

# Understanding the Syntax

```md
![Alt Text](Image URL)
```

- `!` tells Markdown this is an image.
- `[]` contains alternative text.
- `()` contains the image location.

---

# Alternative Text (Alt Text)

Alternative text describes the image.

Example:

```md
![Bella Voice Assistant Logo](assets/logo.png)
```

If the image cannot load, the alternative text is displayed instead.

Alt text is also important for accessibility because screen readers use it to describe images to visually impaired users.

---

# Local Images

Most repositories store images inside an `assets` folder.

Example project structure:

```text
project/

README.md

assets/

logo.png

dashboard.png

demo.gif
```

You can display them using:

```md
![Logo](assets/logo.png)
```

This is the recommended approach.

---

# Remote Images

You can also load images from the internet.

Example:

```md
![Python Logo](https://www.python.org/static/community_logos/python-logo.png)
```

GitHub downloads and displays the image automatically.

---

# Which Should You Use?

Local Images

✅ Always available

✅ Work offline

✅ Version controlled

Remote Images

✅ No repository storage

❌ May disappear if the external website changes

For project documentation, local images are usually the better choice.

---

# Supported Image Formats

GitHub supports several common image formats.

| Format | Supported |
|---------|-----------|
| PNG | ✅ |
| JPG | ✅ |
| JPEG | ✅ |
| GIF | ✅ |
| SVG | ✅ |
| WEBP | ✅ |

PNG is commonly used for screenshots.

SVG is ideal for logos and icons because it scales without losing quality.

---

# Adding GIFs

GIFs are perfect for demonstrating how your application works.

Example:

```md
![Demo](assets/demo.gif)
```

Instead of describing a workflow in several paragraphs, a short GIF often explains everything in a few seconds.

---

# Clickable Images

Images can also act as links.

Syntax:

```md
[![Logo](assets/logo.png)](https://github.com)
```

Clicking the image opens the specified website.

This is commonly used for logos and badges.

---

# Resizing Images

Standard Markdown does **not** support resizing images.

Instead, use HTML.

Example:

```html
<img src="assets/logo.png" width="300">
```

You can also specify height.

```html
<img src="assets/logo.png" width="300" height="200">
```

GitHub supports this.

---

# Aligning Images

Markdown itself doesn't support alignment.

Use HTML.

Center an image:

```html
<p align="center">
    <img src="assets/logo.png" width="250">
</p>
```

Right align:

```html
<p align="right">
    <img src="assets/logo.png" width="250">
</p>
```

---

# Adding Captions

Markdown doesn't provide image captions.

Instead, place text below the image.

Example:

```md
![Dashboard](assets/dashboard.png)

*Figure 1: Main Dashboard*
```

---

# Organizing Images

Instead of placing images randomly throughout your repository, keep them inside an `assets` folder.

Example:

```text
project/

assets/

logo.png

banner.png

dashboard.png

architecture.png

demo.gif

README.md
```

This keeps the repository organized and makes image paths predictable.

---

# Screenshots

Screenshots are one of the best ways to showcase your project.

Example:

```md
## Screenshots

![Home Screen](assets/home.png)

![Settings](assets/settings.png)
```

Readers immediately understand what your application looks like.

---

# Side-by-Side Images

Markdown cannot place images side by side.

Instead, use HTML.

```html
<p align="center">
    <img src="assets/home.png" width="45%">
    <img src="assets/settings.png" width="45%">
</p>
```

This creates a cleaner layout for comparisons.

---

# Images in Tables

Images can also be placed inside Markdown tables.

Example:

```md
| Light Mode | Dark Mode |
|------------|-----------|
| ![](assets/light.png) | ![](assets/dark.png) |
```

This is useful when comparing interfaces.

---

# Best Practices

✔ Store images inside an `assets` folder.

✔ Use descriptive file names.

✔ Compress large images.

✔ Prefer PNG for screenshots.

✔ Prefer SVG for logos.

✔ Add alternative text.

✔ Keep screenshots up to date.

---

# Common Mistakes

## Storing Images Everywhere

❌

```text
README.md

logo.png

image1.png

test.png

photo.png
```

Better:

```text
README.md

assets/

logo.png

dashboard.png

demo.gif
```

---

## Huge Images

Large screenshots make the README difficult to read.

Resize them using HTML.

---

## Missing Alt Text

❌

```md
![](assets/logo.png)
```

Better:

```md
![Project Logo](assets/logo.png)
```

---

## Using Low-Quality Screenshots

Blurry screenshots make a project look unfinished.

Always capture images at a good resolution.

---

# Real Project Example

Imagine your Bella Voice Assistant repository.

```text
Bella/

README.md

assets/

logo.png

demo.gif

dashboard.png

workflow.png
```

README:

```md
# Bella Voice Assistant

![Bella Logo](assets/logo.png)

## Demo

![Demo](assets/demo.gif)

## Screenshots

![Dashboard](assets/dashboard.png)
```

Simple, organized, and professional.

---

# Did You Know?

GitHub caches images for faster loading.

If you replace an image with the same filename, the updated version may not appear immediately because of browser caching.

Refreshing the page or using a private browsing window often helps.

---

# Pro Tip

Instead of filling your README with many screenshots, include:

- One project logo
- One banner (optional)
- One or two screenshots
- One short demo GIF

This provides enough visual context without overwhelming readers.

---

# Mini Exercise

Create a README section that contains:

- A project logo
- A screenshot
- A clickable image
- A centered image

Try writing it before viewing the solution.

<details>

<summary>Solution</summary>

````md
# My Project

![Logo](assets/logo.png)

## Screenshot

![Dashboard](assets/dashboard.png)

## Website

[![Visit Website](assets/logo.png)](https://example.com)

<p align="center">
    <img src="assets/dashboard.png" width="500">
</p>
