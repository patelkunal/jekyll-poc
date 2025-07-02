# Jekyll POC with Minimal Theme

A Jekyll site using the [pages-themes/minimal](https://github.com/pages-themes/minimal) theme, designed for GitHub Pages.

This is developed using copilot extensively.

## Pre-requisites for local development
Note: This is not mandatory step for regular activities. Only if you aim to run this site locally and see its working in your local machine. It is observed that windows is not preferred environment for Jekyll so preferrably use any Unix/Linux based systems or use WSL.

Assuming, WSL's Ubuntu environment is used
1. Update apt index
   ```bash
   sudo apt update
   ```
2. Install ruby and required build dependencies 
   ```bash
   sudo apt install ruby-full build-essential zlib1g-dev
   ```
3. Setup PATH environments - `$HOME/gems/bin` to your path environment
4. Install Jekyll
   ```bash
   gem install jekyll bundler
   ```

## Quick Start

1. **Clone this repository**
   ```bash
   git clone https://github.com/your-username/jekyll-poc.git
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
5. Your site will be available at `https://your-username.github.io/jekyll-poc`

## Theme Information

This site uses the **pages-themes/minimal@v0.2.0** theme, which provides:

- Clean, minimal design
- Responsive layout
- SEO optimization
- GitHub Pages compatibility
- Easy customization

## File Structure

```
├── _config.yml          # Jekyll configuration
├── _posts/              # Blog posts
├── _layouts/            # Page layouts (inherited from theme)
├── index.md             # Homepage
├── about.md             # About page
├── posts.md             # Posts listing page
├── Gemfile              # Ruby dependencies
└── .github/workflows/   # GitHub Actions for deployment
```

## Customization

To customize your site:

1. **Update `_config.yml`** with your site information
2. **Edit pages** in the root directory (index.md, about.md, etc.)
3. **Add new posts** in the `_posts` directory
4. **Customize styling** by creating `assets/css/style.scss`

## Adding Content

### New Posts
Create a new file in `_posts/` with the format: `YYYY-MM-DD-title.markdown`

### New Pages
Create a new `.md` file in the root directory with front matter.

## Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Minimal Theme Repository](https://github.com/pages-themes/minimal)