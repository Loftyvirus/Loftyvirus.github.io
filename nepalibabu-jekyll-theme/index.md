---
title: Nepali Babu Jekyll Theme
description: A theme based on jekyll for documenting stuffs or blog posting
layout: libdoc/page
order: 3
---

A Jekyll-based theme designed for documenting content or blog posting. This guide provides a clear and concise overview of the theme's structure and customization options.

## Table of Contents

1. [Repository](#repository)
2. [Theme Structure](#theme-structure)
3. [Creating a Post](#creating-a-post)
4. [Customizing Styles](#customizing-styles)
5. [Adding JavaScript](#adding-javascript)
6. [Gallery Management](#gallery-management)
7. [Notes](#notes)

---

## Repository

The GitHub repository for this theme can be found here:  
[**Nepali Babu Jekyll Theme**](https://github.com/Loftyvirus/nepalibabu-nepali)

---

## Theme Structure

The theme is organized into the following directories:

| Directory    | Purpose                                                             |
| ------------ | ------------------------------------------------------------------- |
| `_layouts/`  | Contains wrapper templates. `default.html` is the main layout file. |
| `_includes/` | Holds reusable components that are included in layouts.             |
| `_posts/`    | Stores blog posts in Markdown format.                               |
| `_sass/`     | Contains SCSS files for custom styling.                             |
| `assets/`    | Stores compiled CSS, JavaScript, images, and other static files.    |

---

## Creating a Post

To create a new post, add a Markdown file in the `_posts/` directory with the following naming convention:  
`YYYY-MM-DD-post-title.md`

### Example Post

Create a file: `_posts/2025-03-15-my-first-post.md`  
Add the following front matter:

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

2. Compile the SCSS file to CSS using the following command:

   ```bash
   sass _sass/_rightbar.scss assets/css/rightbar.css
   ```

3. Include the compiled CSS file in the `default.html` layout to apply your custom styles.

---

## Adding JavaScript

To add custom JavaScript functionality:

1. Place your JavaScript files in the `assets/scripts/` directory.
2. Include the script in the `default.html` layout using the following syntax:
   ```html
   <script src="/assets/scripts/your-script.js"></script>
   ```
   _or for best practice use relative url as other script example in the same default.html_

---

## Gallery Management

The `assets/gallery/` directory is used to store images, logos, and other media.

- Add your files to this directory.
- Update the `gallery.html` layout to customize paths and display options.

---

## Notes
- install all the dependacies from gem file
- A clean cheat sheet will be provided in the future for easier public use.
- Feel free to modify, delete, or update the repository to suit your needs.
- also update the \_config.yml as well according yo your preferences
