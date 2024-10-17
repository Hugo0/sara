# Sara Perestrelo's Blog

This is the source code for Sara Perestrelo's personal blog, built with Hugo and the Typo theme.

## Prerequisites

Before you begin, ensure you have the following installed on your system:

1. [Hugo](https://gohugo.io/getting-started/installing/) (Extended version)
2. [Git](https://git-scm.com/downloads)

## Getting Started

To run this website locally for development, follow these steps:

1. Clone the repository:

   ```
   git clone https://github.com/Hugo0/sara.git
   cd sara
   ```

2. Install the theme (if not already included):

   ```
   git submodule add https://github.com/tomfran/typo themes/Typo
   ```

3. Start the Hugo development server:

   ```
   hugo server -D
   ```

4. Open your browser and navigate to `http://localhost:1313` to view the website.

The `-D` flag includes draft content. Hugo will watch for changes and automatically refresh the browser.

## Creating New Content

To create a new blog post:

1. Use the Hugo command to generate a new post file:

   ```
   hugo new content posts/my-new-post.md
   ```

   This will create a new Markdown file in the `content/posts/` directory with some default front matter.

2. Open the newly created file (e.g., `content/posts/my-new-post.md`) in your preferred text editor.

3. Edit the front matter at the top of the file. It will look something like this:

   ```yaml
   +++
   title = 'My New Post'
   date = 2023-07-14T12:34:56+01:00
   draft = true
   +++
   ```

   Modify the title as needed, and set `draft = false` when you're ready to publish.

4. Write your blog post content below the front matter using Markdown syntax.

5. Save the file.

6. Run `hugo server` to preview your site locally and ensure the new post appears as expected.

7. When you're satisfied with your post, commit the new file to your Git repository and push it to GitHub:

   ```
   git add content/posts/my-new-post.md
   git commit -m "Add new blog post: My New Post"
   git push origin main
   ```

8. The GitHub Actions workflow will automatically build and deploy your updated site.

## Editing Content

1. Navigate to the `content/` directory.
2. Open the desired Markdown file in your preferred text editor.
3. Edit the front matter (the YAML or TOML block at the top of the file) to set metadata like title, date, and tags.
4. Write your content using Markdown syntax below the front matter.

Example of a post's front matter and content:

```markdown
---
title: "My First Blog Post"
date: 2023-04-15T10:00:00-07:00
draft: false
tags: ["hugo", "blogging"]
---

# Welcome to my blog!

This is the content of my first blog post. You can use **Markdown** syntax here.
```

## Adding Images

1. Place your images in the `static/images/` directory.
2. Reference them in your Markdown content like this:

```markdown
![Alt text](/images/my-image.jpg)
```

## Creating Pages

To create a new page (not a blog post):

```
hugo new content about.md
```

This will create a new page at `content/about.md`.

## Customizing the Theme

1. To override theme templates, copy the file you want to modify from `themes/Typo/layouts/` to your site's `layouts/` directory.
2. Edit the copied file to make your changes.
3. Hugo will use your custom version instead of the theme's version.

## Deployment

This site is set up to deploy automatically when changes are pushed to the main branch. The deployment process is handled by GitHub Actions.

To manually trigger a deployment:

1. Commit your changes and push to the main branch:

   ```
   git add .
   git commit -m "Update site content"
   git push origin main
   ```

2. The GitHub Actions workflow will automatically build and deploy the site.

## Troubleshooting

If you encounter any issues:

1. Ensure Hugo is installed correctly and is the extended version.
2. Check that all theme files are present in the `themes/Typo/` directory.
3. Verify that your content files are in the correct locations.
4. Run `hugo --verbose` to get more detailed output for debugging.

For more help, consult the [Hugo documentation](https://gohugo.io/documentation/) or open an issue in this repository.
