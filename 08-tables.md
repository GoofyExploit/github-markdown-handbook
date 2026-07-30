# Chapter 8 — Tables

Tables are one of the best ways to organize structured information in Markdown.

Instead of presenting data as long paragraphs or lists, tables allow readers to compare information quickly.

GitHub Flavored Markdown (GFM) includes built-in support for tables, making them ideal for documentation, feature comparisons, API references, and project information.

By the end of this chapter, you'll learn:

- Creating tables
- Table syntax
- Column alignment
- Formatting inside tables
- Tables with links
- Tables with images
- Tables with emojis
- Best practices
- Common mistakes

---

# Why Use Tables?

Imagine explaining supported operating systems like this:

- Windows is supported.
- Linux is supported.
- macOS is supported.

Now compare it with:

| Operating System | Supported |
|------------------|-----------|
| Windows | ✅ |
| Linux | ✅ |
| macOS | ✅ |

The table is easier to scan and compare.

---

# Creating a Table

A Markdown table consists of:

- Header row
- Separator row
- Data rows

Syntax:

```md
| Name | Age |
|------|-----|
| Alice | 22 |
| Bob | 25 |
```

Output:

| Name | Age |
|------|-----|
| Alice | 22 |
| Bob | 25 |

---

# Understanding the Syntax

```md
| Column 1 | Column 2 |
|----------|----------|
| Data | Data |
```

- `|` separates columns.
- `-` creates the header separator.
- Each row must have the same number of columns.

---

# Multiple Columns

Example:

```md
| Name | Language | Experience |
|------|----------|------------|
| Lucky | Python | Intermediate |
| Alex | Java | Beginner |
| Emma | C++ | Advanced |
```

Output:

| Name | Language | Experience |
|------|----------|------------|
| Lucky | Python | Intermediate |
| Alex | Java | Beginner |
| Emma | C++ | Advanced |

---

# Column Alignment

By default, text is left-aligned.

Markdown allows three alignment options.

## Left Alignment

```md
| Name | Age |
|:-----|:----|
| Alice | 22 |
```

Output:

| Name | Age |
|:-----|:----|
| Alice | 22 |

---

## Center Alignment

```md
| Name | Age |
|:----:|:---:|
| Alice | 22 |
```

Output:

| Name | Age |
|:----:|:---:|
| Alice | 22 |

---

## Right Alignment

```md
| Name | Salary |
|-----:|-------:|
| Alice | $2,500 |
| Bob | $3,100 |
```

Output:

| Name | Salary |
|-----:|-------:|
| Alice | $2,500 |
| Bob | $3,100 |

---

# Formatting Inside Tables

Markdown formatting works inside table cells.

Example:

```md
| Feature | Status |
|---------|--------|
| **Authentication** | ✅ |
| *Dark Mode* | ❌ |
| `Docker` | ⏳ |
```

Output:

| Feature | Status |
|---------|--------|
| **Authentication** | ✅ |
| *Dark Mode* | ❌ |
| `Docker` | ⏳ |

---

# Links Inside Tables

Links can be placed inside tables.

Example:

```md
| Resource | Link |
|----------|------|
| Python | [Website](https://python.org) |
| GitHub | [Website](https://github.com) |
```

Output:

| Resource | Link |
|----------|------|
| Python | [Website](https://python.org) |
| GitHub | [Website](https://github.com) |

---

# Images Inside Tables

Images can also be used.

Example:

```md
| Light Mode | Dark Mode |
|------------|-----------|
| ![](assets/light.png) | ![](assets/dark.png) |
```

This is useful when comparing application interfaces.

---

# Emojis Inside Tables

Emojis improve readability.

Example:

```md
| Feature | Status |
|---------|--------|
| Login | ✅ |
| Registration | ✅ |
| Docker | ⏳ |
| CI/CD | ❌ |
```

Output:

| Feature | Status |
|---------|--------|
| Login | ✅ |
| Registration | ✅ |
| Docker | ⏳ |
| CI/CD | ❌ |

---

# Code Inside Tables

Inline code works perfectly.

Example:

```md
| Command | Description |
|---------|-------------|
| `git clone` | Clone a repository |
| `git status` | Show repository status |
| `git push` | Upload commits |
```

Output:

| Command | Description |
|---------|-------------|
| `git clone` | Clone a repository |
| `git status` | Show repository status |
| `git push` | Upload commits |

---

# Tables for Feature Comparison

One of the most common uses of tables.

Example:

```md
| Feature | Free | Pro |
|---------|:----:|:---:|
| Unlimited Projects | ❌ | ✅ |
| Team Collaboration | ❌ | ✅ |
| Priority Support | ❌ | ✅ |
```

---

# Tables for Project Information

Example:

```md
| Property | Value |
|----------|-------|
| Language | Python |
| Framework | FastAPI |
| Database | PostgreSQL |
| License | MIT |
```

---

# Tables for API Documentation

Example:

```md
| Endpoint | Method | Description |
|----------|--------|-------------|
| `/users` | GET | Get all users |
| `/users` | POST | Create user |
| `/users/{id}` | DELETE | Delete user |
```

---

# Tables for Keyboard Shortcuts

Example:

```md
| Shortcut | Action |
|----------|--------|
| Ctrl + C | Copy |
| Ctrl + V | Paste |
| Ctrl + Z | Undo |
```

---

# Limitations of Markdown Tables

Markdown tables are simple by design.

They **cannot**:

- Merge cells
- Span multiple columns
- Span multiple rows
- Automatically wrap complex layouts
- Resize columns manually

For advanced layouts, use HTML instead.

---

# Best Practices

✔ Keep tables simple.

✔ Use short column names.

✔ Align numeric data to the right.

✔ Keep related information together.

✔ Use emojis sparingly.

✔ Prefer tables only when comparing structured information.

---

# Common Mistakes

## Too Many Columns

❌

```text
| A | B | C | D | E | F | G | H | I |
```

Readers will have to scroll horizontally.

Keep tables compact.

---

## Using Tables for Long Paragraphs

Tables are for structured data.

If each cell contains a paragraph, a normal section is usually easier to read.

---

## Inconsistent Columns

❌

```md
| Name | Age |
|------|-----|
| Alice |
```

Every row should have the same number of columns.

---

## Missing Header Separator

❌

```md
| Name | Age |
| Alice | 22 |
```

Always include the separator row.

---

# Real Project Example

Imagine you're documenting the **Bella Voice Assistant**.

```md
## Features

| Feature | Available |
|----------|:---------:|
| AI Chat | ✅ |
| Wake Word Detection | ✅ |
| News Reader | ✅ |
| Music Player | ✅ |
| Calendar | ⏳ |
| Email Support | ❌ |

## Technologies

| Component | Technology |
|-----------|------------|
| Language | Python |
| Speech Recognition | SpeechRecognition |
| TTS | Kokoro |
| AI | OpenAI API |
| News | NewsAPI |
```

This gives readers a quick overview of your project.

---

# Did You Know?

GitHub automatically adjusts column widths based on the content.

You don't need to perfectly align the `|` characters in your source code, although many developers do so because it improves readability.

---

# Pro Tip

Use tables only when readers need to compare information.

If you're simply listing items, a bullet list is usually the better choice.

---

# Mini Exercise

Create a table showing:

- Three programming languages
- Their primary use
- Difficulty level

Try it before viewing the solution.

<details>

<summary>Solution</summary>

```md
| Language | Primary Use | Difficulty |
|----------|-------------|------------|
| Python | Automation | Easy |
| JavaScript | Web Development | Medium |
| Rust | Systems Programming | Hard |
```

</details>

---

# Quick Quiz

### 1. Which character separates table columns?

A. `:`

B. `|`

C. `-`

**Answer:** **B**

---

### 2. How do you center-align a column?

A.

```md
|:---:|
```

B.

```md
|---:|
```

C.

```md
|:---|
```

**Answer:** **A**

---

### 3. Can Markdown tables merge cells?

**Answer:** No. Use HTML for complex table layouts.

---

# Summary

In this chapter, you learned:

- How to create tables
- Column alignment
- Formatting inside tables
- Links, images, and code in tables
- Common use cases
- Limitations
- Best practices

Tables are an excellent way to present structured information clearly and professionally.

---

# Key Takeaways

- Use tables for structured data.
- Keep them simple and readable.
- Align numeric data appropriately.
- Don't force long text into table cells.
- Use HTML when you need advanced layouts.

---

# Next Chapter

➡ **Chapter 9 — Blockquotes & GitHub Alerts**

In the next chapter, you'll learn how to create blockquotes, nested quotes, callouts, notes, warnings, tips, and GitHub's built-in alert syntax to make important information stand out.
