# ItWorksGlobalSolutions Website

This is the official website for ItWorksGlobalSolutions, built with Jekyll and hosted on GitHub Pages.

## Setup Instructions

1. This repository is set up for GitHub Pages.
2. Custom domain: itwgs.com (configured via CNAME file)
3. To enable GitHub Pages:
   - Go to repository Settings > Pages
   - Set source to "Deploy from a branch"
   - Branch: main, Folder: /(root)
   - For custom domain, enter "itwgs.com" in the custom domain field

## DNS Configuration

To use the custom domain, configure your DNS provider (for itwgs.com) with the following records provided by GitHub Pages settings.

## Local Development

To run locally:

```bash
bundle install
bundle exec jekyll serve
```

Visit `http://localhost:4000` to preview the site.

## Content

- Home page: Overview of services
- About: Company information
- Contact: Contact form and details

## Technologies

- Jekyll (static site generator)
- Minima theme
- Hosted on GitHub Pages