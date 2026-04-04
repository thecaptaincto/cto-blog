# Formatting Guide — Voices of the World

Everything you need to write and publish a new post yourself.

---

## Quick Reference

| What you want | HTML tag | Example |
|---|---|---|
| Paragraph | `<p>` | `<p>Your text.</p>` |
| Main section heading | `<h2>` | `<h2>Title</h2>` |
| Subsection heading | `<h3>` | `<h3>Subtitle</h3>` |
| **Bold** | `<strong>` | `<strong>word</strong>` |
| *Italic* | `<em>` | `<em>word</em>` |
| Bullet list | `<ul>` + `<li>` | see below |
| Numbered list | `<ol>` + `<li>` | see below |
| Pull quote | `<blockquote>` | see below |
| Line break | `<br>` | `first line<br>second line` |
| Link | `<a href="">` | see below |

---

## Templates

### New French post (`french/my-post.html`)

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Post Title - Voices of the World</title>
    <link rel="stylesheet" href="../style.css">
</head>
<body>
    <div class="ink-splash"></div>

    <header class="article-header">
        <a href="../index.html" class="back-link">← Accueil</a>
        <div class="brush-stroke"></div>
        <h1>Post Title</h1>
        <p class="article-meta">Subtitle or short description</p>
    </header>

    <article class="article-content">
        <p class="drop-cap">First paragraph — gets the large drop-cap letter automatically.</p>

        <p>Second paragraph.</p>

        <h2>Section Title</h2>

        <p>Section content...</p>

        <h3>Subsection Title</h3>

        <p>More content...</p>
    </article>
</body>
</html>
```

### New English accent post (`english-accents/my-post.html`)

Same template as above, but change:
- `<html lang="fr">` → `<html lang="en">`
- `← Accueil` → `← Home`

Everything else is identical (`../style.css`, `../index.html`).

---

## Formatting Elements

### Paragraphs

Every block of text needs `<p>` tags. Don't leave bare text floating in the article.

```html
<p>This is a paragraph.</p>

<p>This is another paragraph. It will have proper spacing above it automatically.</p>
```

### Section Headers

Use `<h2>` for main sections, `<h3>` for subsections within a section. Never use `<h1>` inside an article — that's reserved for the page title in the header.

```html
<h2>Main Section</h2>

<p>Content under this section...</p>

<h3>A Subsection</h3>

<p>More detailed content...</p>
```

`h2` automatically gets a bottom border line. `h3` is automatically italicised.

### Bold and Italic

```html
<p>Use <strong>bold</strong> for key terms, names, or emphasis that matters.</p>

<p>Use <em>italic</em> for foreign words, titles, or softer emphasis.</p>

<p>You can combine them: <strong><em>bold italic</em></strong>.</p>
```

### Lists

**Bullet list:**
```html
<ul>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ul>
```

**Numbered list:**
```html
<ol>
    <li>First step</li>
    <li>Second step</li>
    <li>Third step</li>
</ol>
```

Use a list when you have 3 or more items. Fewer than 3, just write them in a sentence.

### Blockquotes

For pull quotes, important passages, or anything you want visually set apart. The `"` large quotation mark appears automatically.

```html
<blockquote>
    This is a memorable quote or important statement. It will be styled with
    a large opening quote mark and a left border.
</blockquote>
```

Use sparingly — one or two per article at most.

### Links

```html
<p>Read more about this on <a href="https://example.com">this page</a>.</p>
```

To link to another post on the blog (from within a subfolder):
```html
<a href="../french/montreal.html">my Montréal article</a>
```

---

## The Drop Cap

The first paragraph of every article should have `class="drop-cap"` to get the large decorative first letter:

```html
<article class="article-content">
    <p class="drop-cap">This first paragraph gets a large drop cap on the first letter automatically...</p>

    <p>The second paragraph is normal.</p>
```

Only use `drop-cap` once, on the very first paragraph.

---

## Adding a New Post to the Homepage

Open `index.html`. Find the right `<nav class="post-grid">` section (there are two — one for English, one for French) and add a new card at the end of that nav block.

**Card format:**
```html
<a href="french/my-post.html" class="post-card">
    <div class="card-number">04</div>
    <h2>Post Title</h2>
    <p>One or two sentences describing what the post is about.</p>
    <div class="ink-line"></div>
</a>
```

- Set `card-number` to the next number in that section
- For English posts: `href="english-accents/my-post.html"`
- For French posts: `href="french/my-post.html"`

---

## Common Mistakes

**Wrong path for stylesheet** — posts in subfolders need `../`:
```html
<!-- WRONG (will break all styling) -->
<link rel="stylesheet" href="style.css">

<!-- CORRECT -->
<link rel="stylesheet" href="../style.css">
```

**Wrong path for back link:**
```html
<!-- WRONG -->
<a href="index.html" class="back-link">← Home</a>

<!-- CORRECT -->
<a href="../index.html" class="back-link">← Home</a>
```

**Using h1 inside the article** — don't. The `<h1>` only goes in the `<header>` block at the top of the page.

**Forgetting to close tags** — every `<p>` needs a `</p>`, every `<strong>` needs a `</strong>`, etc.

**Not adding the card to index.html** — creating the HTML file isn't enough. You also need to add the card manually to `index.html` or the post won't be linked from anywhere.

---

## Language Attribute

Set the correct language on the `<html>` tag so the browser knows what language the page is in:

```html
<html lang="fr">   <!-- French posts -->
<html lang="en">   <!-- English posts -->
```

---

## Checklist for a New Post

- [ ] Created the HTML file in the right folder (`french/` or `english-accents/`)
- [ ] Used `../style.css` in the `<link>` tag
- [ ] Used `../index.html` in the back link
- [ ] Set correct `lang` attribute on `<html>`
- [ ] First `<p>` has `class="drop-cap"`
- [ ] Used `<h2>` / `<h3>` for sections (not `<h1>`)
- [ ] Added a card in `index.html` with the correct `href` and next card number
