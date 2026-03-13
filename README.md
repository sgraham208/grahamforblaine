# GrahamForBlaine.com

Campaign website for Stephen Graham, Blaine County Clerk.

## File Structure

```
├── index.html          ← Main English site (single file, all CSS/JS inline)
├── es/
│   └── index.html      ← Spanish language page (translation placeholders)
├── logo_white.png      ← Site logo (you provide this)
├── headshot.jpg         ← Headshot photo (you provide this)
└── README.md
```

## Hosting on GitHub Pages

1. Create a repository (e.g. `grahamforblaine.com`)
2. Push these files to the `main` branch
3. Go to **Settings → Pages** → set source to `main` branch, root `/`
4. Under **Custom domain**, enter `grahamforblaine.com`
5. Add a `CNAME` file with `grahamforblaine.com` (GitHub can do this automatically)
6. At your DNS provider, point `grahamforblaine.com` to GitHub Pages:
   - **A records** → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - **CNAME** for `www` → `<your-username>.github.io`

## How to Update

All content is plain HTML — edit `index.html` directly on GitHub or in any text editor.

### Common edits:

- **Change text**: Find the section in `index.html`, edit the text between the HTML tags
- **Add a "What We've Built" item**: Copy an existing `<article class="built-item">` block and change the heading and paragraph
- **Update the About section**: Find `<!-- ===== About Stephen -->` and edit the `<p>` tags
- **Spanish page**: Replace the placeholder notices in `es/index.html` with translated content from your translator. The English source text is in HTML comments right below each placeholder.

### Spanish page workflow:

1. Send the English text (visible in HTML comments in `es/index.html`) to your translator
2. When translations come back, replace each `<p class="translation-notice">` block with the translated `<h3>` and `<p>` content
3. Remove or keep the English HTML comments as you prefer

## Images

You'll need to provide two image files in the root directory:

- `logo_white.png` — white logo for the header and footer
- `headshot.jpg` — Stephen's headshot photo

## Design Notes

- **Fonts**: Playfair Display (headings) + Source Sans 3 (body) — loaded from Google Fonts
- **Colors**: Navy/blue civic palette — all defined as CSS variables at the top of `index.html`
- **Dark mode**: Automatic via `prefers-color-scheme`
- **Responsive**: Works on phones (375px) through desktop (1440px+)
- **Accessibility**: WCAG 2.1 AA — proper contrast, keyboard navigation, semantic HTML
