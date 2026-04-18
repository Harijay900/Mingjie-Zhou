# Mingjie Zhou Homepage

This is an English academic homepage built with Jekyll and a compact single-page layout inspired by Jon Barron's homepage.

## Deploy on GitHub Pages

1. Create a repository named `your-github-username.github.io`.
2. Push all files in this directory to the repository.
3. Open `Settings -> Pages`.
4. Select `Deploy from a branch`, branch `main`, folder `/ (root)`.
5. Wait for GitHub Pages to build the site.

## Local Preview

Local preview requires Ruby, Bundler, and Jekyll.

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## Content

- Main content: `index.md`
- Site configuration: `_config.yml`
- Publications: `_data/publications.yml`
- Profile image: `assets/img/avatar-placeholder.svg`
- Main stylesheet: `assets/css/barron.css`
