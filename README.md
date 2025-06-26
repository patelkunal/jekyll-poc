# Jekyll POC with Simplex Theme

A Jekyll site using the [andreondra/jekyll-theme-simplex](https://github.com/andreondra/jekyll-theme-simplex) theme, designed for GitHub Pages.

## Quick Start

1. **Clone this repository**
   ```bash
   git clone https://github.com/patelkunal/jekyll-poc.git
   cd jekyll-poc
   ```

2. **Install dependencies**
   ```bash
   bundle install
   ```

3. **Run locally**
   ```bash
   bundle exec jekyll serve
   ```

4. **Visit your site**
   Open [http://localhost:4000](http://localhost:4000) in your browser

## GitHub Pages Setup

This repository is configured to deploy automatically to GitHub Pages using GitHub Actions:

1. Go to your repository settings
2. Navigate to "Pages" in the sidebar
3. Under "Source", select "GitHub Actions"
4. Push your changes to the `main` branch
5. Your site will be available at `https://patelkunal.github.io/jekyll-poc`

## Theme Information

This site uses the **andreondra/jekyll-theme-simplex** theme, which provides:

- Modern, clean design with light/dark mode support
- Fully responsive layout
- Category and author system
- Image lightbox functionality
- SEO optimization
- GitHub Pages compatibility

## Features

✅ **🌓 Dark Mode** - Automatic light/dark theme switching  
✅ **📱 Responsive** - Perfect on all screen sizes  
✅ **🏷️ Categories** - Organize posts by categories  
✅ **👤 Authors** - Support for multiple authors with profiles  
✅ **🖼️ Lightbox** - Beautiful image viewing experience  
✅ **🚀 Fast** - Optimized for performance  
✅ **🔍 SEO** - Built-in SEO optimization  

## File Structure

```
├── _config.yml          # Jekyll configuration
├── _data/               # Site data (navigation, etc.)
├── _posts/              # Blog posts
├── _category/           # Category definitions
├── _authors/            # Author profiles
├── index.md             # Homepage (uses home layout)
├── about.md             # About page
├── posts.md             # Posts listing page
├── Gemfile              # Ruby dependencies
└── .github/workflows/   # GitHub Actions for deployment
```

## Customization

To customize your site:

1. **Update `_config.yml`** with your site information
2. **Configure navigation** in `_data/nav.yaml`
3. **Add categories** in the `_category` directory
4. **Add authors** in the `_authors` directory
5. **Edit pages** in the root directory (index.md, about.md, etc.)
6. **Add new posts** in the `_posts` directory

## Adding Content

### New Posts
Create a new file in `_posts/` with the format: `YYYY-MM-DD-title.markdown`

Required front matter:
```yaml
---
layout: post
title: "Your Post Title"
date: 2025-06-26 00:00:00 +0000
category: [category1, category2]
author: author_nick
---
```

### New Categories
Create a new file in `_category/` with:
```yaml
---
category: [your-category]
hue: var(--c-themeHueBlue)
title: Category Title
description: Category description
---
```

### New Authors
Create a new file in `_authors/` with:
```yaml
---
nick: author_nick
full_name: Author Full Name
photo_dir: assets/img/authors/author.png
---
```

## Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Simplex Theme Repository](https://github.com/andreondra/jekyll-theme-simplex)
- [Simplex Theme Demo](https://simplex-demo.golas.systems/)