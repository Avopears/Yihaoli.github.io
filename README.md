# Yihao Li — Personal Academic Homepage

This repository contains a GitHub Pages/Jekyll academic homepage based on the [Minimal Light](https://github.com/yaoyao-liu/minimal-light) theme family.

## Personalize the site

1. Edit `_config.yml` to update the name, position, institution, email, profile links, and site metadata.
2. Replace the placeholder sections in `index.md` with the real biography, interests, education, experience, projects, awards, and skills.
3. Add publication records to `_data/publications.yml` using the commented example in that file.
4. Put a portrait in `assets/img/` and set `avatar` in `_config.yml`, for example `avatar: assets/img/avatar.jpg`.
5. Put the CV and papers in `assets/files/`, then link them from `_config.yml` or `_data/publications.yml`.

## Preview locally

Install Ruby, then run:

```bash
bundle install
bundle exec jekyll serve
```

Open `http://localhost:4000/Yihaoli.github.io/`.

## Publish with GitHub Pages

In the repository settings, open **Pages** and choose **Deploy from a branch**, then select the default branch and `/ (root)`.

Because this repository is named `Yihaoli.github.io` under the `Avopears` account, its default project-site address is:

`https://avopears.github.io/Yihaoli.github.io/`

To publish at `https://avopears.github.io/`, rename the repository to `Avopears.github.io` and update `baseurl` and `canonical` in `_config.yml`.

