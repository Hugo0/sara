# Sara Perestrelo's Blog

This is the source code for Sara Perestrelo's personal blog, built with Hugo and the Typo theme.

## Prerequisites

Before you begin, ensure you have [Hugo Extended](https://gohugo.io/getting-started/installing/) installed on your system as well as [Git]()

## Getting Started

To run this website locally for development:

1. Clone the repository:

   ```bash
   git clone https://github.com/Hugo0/sara.git
   cd sara
   ```

2. Start the Hugo development server:

   ```bash
   hugo server -D
   ```

## Creating Content

### Blog Posts

1. Create a new post:

   ```bash
   hugo new content posts/my-post-name/index.md
   ```

2. For bilingual posts, create both language versions:

   ```bash
   hugo new content posts/my-post-name/index.en.md
   hugo new content posts/my-post-name/index.pt.md
   ```

3. Add your content using Markdown syntax. Example front matter:
   ```yaml
   ---
   title: "My Post Title"
   date: 2024-01-20
   draft: false
   tags: ["tag1", "tag2"]
   giscus_term: "my-post-name-20240120" # Required for comments
   ---
   ```

### Images

1. Place images in your post's directory alongside the markdown file:

   ```
   content/
   └── posts/
       └── my-post-name/
           ├── index.en.md
           ├── index.pt.md
           └── image.jpg
   ```

2. Reference images in your markdown:
   ```markdown
   ![Image description](image.jpg)
   ```

## Deployment

The site is automatically deployed on [Render](https://render.com) to [saraperestrelo.com](https://saraperestrelo.com) when changes are pushed to the main branch.
