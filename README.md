# OC-Dot-In

Personal brand website for Om Chaturvedi (omchaturvedi.in) — a static site, no build step required.

## Structure

```
index.html              # One-page homepage: About, Businesses, Vision, Contact
blog/index.html          # Blog listing page (reads assets/js/posts.js)
blog/posts/_template.html # Copy this to start a new blog post
assets/css/style.css     # All site styles
assets/js/main.js        # Nav toggle + small behaviors
assets/js/posts.js       # Blog post metadata (title, date, excerpt, url)
```

## Running locally

No build tools needed. From the project root:

```
python3 -m http.server 8000
```

Then open http://localhost:8000

## Publishing a new blog post

1. Copy `blog/posts/_template.html` to `blog/posts/your-post-slug.html`.
2. Replace the title, date, and body content in that file.
3. Add an entry to `assets/js/posts.js`:
   ```js
   {
     title: "Your Post Title",
     date: "2026-07-15",
     excerpt: "One or two sentences describing the post.",
     url: "posts/your-post-slug.html",
   }
   ```
4. Commit and push. The post will appear on `/blog/index.html`, newest first.

## Deploying

This is a static site — it can be hosted as-is on GitHub Pages, Netlify, Vercel, or any static host, then pointed at the `omchaturvedi.in` domain.

## Content notes

The About/Businesses/Vision copy was drafted from public information (LinkedIn, Chartered Studies' website, and press coverage) since this was built without an interactive confirmation step. Please review it for accuracy — especially the Pepplo Softwares status (current vs. past venture) — and edit `index.html` directly before publishing.
