---
title: Nepali Babu Jekyll Theme
description: A Jekyll-based theme for documentation or blog posting.
layout: libdoc/page
order: 3
---

A clean and minimal Jekyll theme designed for documentation or blog posting. This guide provides an overview of the theme's structure, customization options, and usage.

---

## Table of Contents

1. [Repository](#repository)
2. [Theme Structure](#theme-structure)
3. [Creating a Post](#creating-a-post)
4. [Customizing Styles](#customizing-styles)
5. [Adding JavaScript](#adding-javascript)
6. [Gallery Management](#gallery-management)
7. [Docker setup](#docker-setup)
8. [Notes](#notes)

---

## Repository

The GitHub repository for this theme is available here:  
[**Nepali Babu Jekyll Theme**](https://github.com/Loftyvirus/nepalibabu-nepali)

---

## Theme Structure

The theme is organized into the following directories:

| Directory    | Purpose                                                             |
| ------------ | ------------------------------------------------------------------- |
| `_layouts/`  | Contains wrapper templates. `default.html` is the main layout file. |
| `_includes/` | Holds reusable components included in layouts.                      |
| `_posts/`    | Stores blog posts in Markdown format.                               |
| `_sass/`     | Contains SCSS files for custom styling.                             |
| `assets/`    | Stores compiled CSS, JavaScript, images, and other static files.    |

---

## Creating a Post

To create a new post, add a Markdown file in the `_posts/` directory with the following naming convention:  
`YYYY-MM-DD-post-title.md`

### Example Post

1. Create a file: `_posts/2025-03-15-my-first-post.md`
2. Add the following front matter:

```markdown
---
layout: post
title: "First Post"
date: 2025-03-15
image: /assets/web/nepalibabufirst.png
excerpt: "The first post of this theme."
---
```

---

## Customizing Styles

1. Create a custom SCSS file in the `_sass/` directory.  
   Example: `_sass/_rightbar.scss`

2. Compile the SCSS file to CSS using:

   ```bash
   sass _sass/_rightbar.scss assets/css/rightbar.css
   ```

3. Include the compiled CSS file in the `default.html` layout to apply your styles.

---

## Adding JavaScript

To add custom JavaScript:

1. Place your JavaScript files in the `assets/scripts/` directory.
2. Include the script in the `default.html` layout:
   ```html
   <script src="/assets/scripts/your-script.js"></script>
   ```
   _For best practices, use relative URLs as shown in the existing scripts in `default.html`._

---

## Gallery Management

The `assets/gallery/` directory stores images, logos, and other media.

1. Add your files to this directory.
2. Update the `gallery.html` layout to customize paths and display options.

---

## Docker Setup

To build and run the Jekyll site using Docker:

```markdown
- docker build -t nepalibabu-jekyll .
- docker run -p 4000:6969 nepalibabu-jekyll
```

Access the site at `http://localhost:4000/`.

---

## Notes

- Install all dependencies from the `Gemfile`.
- A clean cheat sheet will be provided in the future for easier public use.
- Feel free to modify, delete, or update the repository to suit your needs.
- Update `_config.yml` according to your preferences.
