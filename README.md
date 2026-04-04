# Voices of the World — Personal Blog

A personal blog covering language, travel, and life — written in English and French. Hosted on GitHub Pages at [thecaptaincto.github.io/cto-blog](https://thecaptaincto.github.io/cto-blog/).

## What This Blog Is

Two sections, one blog:

- **English Around the World** — long-form explorations of English accents across nine regions. How local languages shape English pronunciation, and what those accents reveal about culture and identity.
- **Écriture en Français** — articles written in French. A space to write seriously in Molière's language, on whatever subject feels worth exploring.

## File Structure

```
cto-blog/
├── index.html              ← Homepage (ocean-themed, two sections)
├── style.css               ← All styling and animations
├── README.md               ← You are here
├── FORMATTING-GUIDE.md     ← How to write and add new posts
│
├── english-accents/        ← English accent articles
│   ├── native-accents.html
│   ├── nordic-accents.html
│   ├── latin-accents.html
│   ├── eastern-european-accents.html
│   ├── middle-eastern-accents.html
│   ├── african-accents.html
│   ├── south-asian-accents.html
│   ├── east-asian-accents.html
│   └── southeast-asian-accents.html
│
└── french/                 ← French-language articles
    ├── cactus.html
    ├── montreal.html
    └── auberges.html
```

**Important:** Posts inside `english-accents/` and `french/` must link to `../style.css` and `../index.html` (note the `../`). Posts at the root would use `style.css` and `index.html` directly.

## Design

- **Homepage** — deep ocean gradient (pale horizon → teal → midnight navy), animated waves, frosted-glass cards
- **Article pages** — clean ink-on-paper aesthetic, serif typography, no ocean theme
- **Fonts** — Crimson Text (body), Noto Serif SC (headers)
- **No JavaScript** — pure HTML and CSS

## Adding New Posts

See `FORMATTING-GUIDE.md` for the full template, formatting reference, and step-by-step instructions for adding posts to either section.

## Publishing

The blog is deployed via GitHub Pages. Push to `main` and changes go live automatically at the URL above.
