# HTML FORMATTING GUIDE FOR YOUR BLOG

This guide explains how to format text in your blog posts using HTML.

## PARAGRAPHS

To create a paragraph, wrap your text in `<p>` tags:

```html
<p>This is a paragraph. It will have spacing above and below it.</p>
```

## HEADERS

Headers create different levels of section titles. Use h2 for main sections and h3 for subsections:

```html
<h2>This is a Main Section Header</h2>
<h3>This is a Subsection Header</h3>
```

Important: Don't use h1 in article content—it's reserved for the page title.

## TEXT FORMATTING

### Bold Text
Wrap text in `<strong>` tags to make it bold:

```html
<p>This is <strong>bold text</strong> in a sentence.</p>
```

### Italic Text
Wrap text in `<em>` tags to make it italic:

```html
<p>This is <em>italic text</em> in a sentence.</p>
```

### Bold AND Italic
You can combine them:

```html
<p>This is <strong><em>bold and italic</em></strong> text.</p>
```

## LISTS

### Bullet Point Lists (Unordered)

```html
<ul>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ul>
```

### Numbered Lists (Ordered)

```html
<ol>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ol>
```

## BLOCKQUOTES

For quotations or special highlighted text:

```html
<blockquote>
    This text will appear as a special quote with styling and quotation marks.
</blockquote>
```

## LINE BREAKS

To create a line break within a paragraph without starting a new paragraph:

```html
<p>First line<br>Second line</p>
```

## LINKS

To create clickable links:

```html
<p>Visit <a href="https://example.com">this website</a> for more info.</p>
```

## COMPLETE EXAMPLE

Here's how all these elements work together in a blog post:

```html
<h2>My Trip to Paris</h2>

<p>Last summer, I visited <strong>San Francisco</strong> for the first time. It was an <em>amazing</em> experience that I'll never forget.</p>

<h3>Places I Visited</h3>

<p>Here are the highlights of my trip:</p>

<ul>
    <li>The Golden Gate Bridge</li>
    <li>Alcatraz Island</li>
    <li>Chinatown</li>
    <li>The Painted Ladies</li>
    <li>Lombard Street</li>
</ul>

<h3>What I Learned</h3>

<p>The most important lesson was:</p>

<blockquote>
    Travel changes you in ways you never expect.
</blockquote>

<p>I would <strong><em>highly recommend</em></strong> San Francisco to anyone!</p>
```

## SPECIAL STYLING ALREADY IN YOUR BLOG

Your blog has special CSS that automatically styles:

- **Drop Cap**: The first paragraph in each article has an automatic large first letter
- **Headers**: h2 gets an underline, h3 is italicized
- **Paragraphs**: Automatically justified and spaced
- **Blockquotes**: Get quotation marks and special styling
- **Lists**: Automatically styled with proper spacing

## CREATING A NEW BLOG POST

To create a new page, follow this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Post Title - Voices of the World</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="ink-splash"></div>
    
    <header class="article-header">
        <a href="index.html" class="back-link">← Home</a>
        <div class="brush-stroke"></div>
        <h1>Your Post Title</h1>
        <p class="article-meta">Your subtitle or description</p>
    </header>

    <article class="article-content">
        <!-- Your content goes here -->
        <p>First paragraph will have a drop cap automatically...</p>
        
        <h2>Section Title</h2>
        <p>Section content...</p>
        
        <h3>Subsection</h3>
        <p>More content...</p>
    </article>
</body>
</html>
```

## ADDING YOUR NEW POST TO THE HOME PAGE

After creating a new post, add it to the navigation on index.html:

Find the `<nav class="post-grid">` section and add:

```html
<a href="your-post-filename.html" class="post-card">
    <div class="card-number">10</div>
    <h2>Your Post Title</h2>
    <p>Brief description of what the post is about</p>
    <div class="ink-line"></div>
</a>
```

## TIPS FOR GOOD FORMATTING

1. **Use paragraphs liberally** - Don't make huge blocks of text
2. **Headers break up content** - Use h2 for major topics, h3 for subtopics
3. **Bold for emphasis** - Use `<strong>` for important terms or concepts
4. **Italic for style** - Use `<em>` for foreign words, book titles, or gentle emphasis
5. **Lists for clarity** - When you have 3+ items, use a list instead of listing in a paragraph
6. **Blockquotes sparingly** - Only for actual quotes or very important statements

Your blog is now ready to use! All the styling is handled automatically by the CSS file.
