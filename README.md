# ItWorksGlobalSolutions Website

Official website for [itwgs.com](https://itwgs.com), built with Jekyll and hosted on GitHub Pages.

---

## 1. Enable GitHub Pages

1. Go to **Settings → Pages** in this repository.
2. Set **Source** → Deploy from a branch → `main` / `/ (root)`.
3. Under **Custom domain**, enter `itwgs.com` and save.
4. Check **Enforce HTTPS** once the domain validates.

---

## 2. DNS Configuration

### itwgs.com (primary domain)

Add these records at your DNS registrar for `itwgs.com`:

| Type  | Host | Value                    |
|-------|------|--------------------------|
| A     | @    | 185.199.108.153          |
| A     | @    | 185.199.109.153          |
| A     | @    | 185.199.110.153          |
| A     | @    | 185.199.111.153          |
| CNAME | www  | itwgs.github.io          |

### itwgs.net (redirect to itwgs.com)

GitHub Pages only supports one custom domain per site. To make `itwgs.net` resolve to the same site, configure a **URL redirect / forwarding** rule at your `itwgs.net` registrar:

- Forward `itwgs.net` → `https://itwgs.com` (301 permanent redirect)
- Forward `www.itwgs.net` → `https://itwgs.com`

Most registrars offer this under "Domain Forwarding" or "URL Redirect" in their DNS settings.

---

## 3. Contact Form (Formspree)

The contact form uses [Formspree](https://formspree.io) — a free backend for static forms:

1. Sign up at https://formspree.io.
2. Create a new form and copy your **Form ID** (looks like `xpzgabcd`).
3. In `contact.markdown`, replace `YOUR_FORM_ID` with your actual form ID:
   ```
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
4. Submissions will be delivered to your Formspree-linked email address.

---

## 4. Local Development

```bash
bundle install
bundle exec jekyll serve
```

Visit `http://localhost:4000` to preview the site.

---

## Structure

| File / Folder      | Purpose                        |
|--------------------|--------------------------------|
| `index.markdown`   | Home page                      |
| `about.markdown`   | About page                     |
| `contact.markdown` | Contact page with form         |
| `CNAME`            | Custom domain (itwgs.com)      |
| `_config.yml`      | Site settings                  |
| `Gemfile`          | Ruby dependencies (github-pages gem) |