# JimmyAkl.github.io

Personal portfolio and blog site for Jimmy Akl, built with Jekyll and hosted on GitHub Pages.

🌐 **Live site**: [https://jimmyakl.github.io](https://jimmyakl.github.io)

## Local Development

### Prerequisites

- Ruby (2.7 or higher)
- Bundler

### Setup

```bash
# Install dependencies
bundle install

# Run the site locally
bundle exec jekyll serve

# The site will be available at http://localhost:4000
```

### Build the site

```bash
bundle exec jekyll build
```

The built site will be in the `_site` directory.

## Adding a New Blog Post

Blog posts are written in Markdown and stored in the `_posts` directory.

### File Naming Convention

Posts must follow this exact naming format:

```
YYYY-MM-DD-title-with-hyphens.md
```

**Examples**:
- `2024-11-10-my-first-post.md`
- `2024-12-25-christmas-thoughts.md`
- `2025-01-15-learning-rust.md`

### Front Matter

Every post must start with YAML front matter between triple dashes:

```yaml
---
layout: post
title: "Your Post Title"
date: 2024-11-10
---
```

### Full Example Post

Create a file `_posts/2024-11-10-my-new-post.md`:

```markdown
---
layout: post
title: "My New Post Title"
date: 2024-11-10
---

This is the first paragraph of your post. You can write in regular Markdown.

## Subheading

More content here. You can use **bold**, *italic*, and [links](https://example.com).

### Code Examples

\`\`\`python
def hello():
    print("Hello, world!")
\`\`\`

### Lists

- Item one
- Item two
- Item three
```

### Adding Images to Posts

1. Create an `assets/images` directory if it doesn't exist:
   ```bash
   mkdir -p assets/images
   ```

2. Add your image files to this directory

3. Reference them in your post:
   ```markdown
   ![Image description](/assets/images/my-image.png)
   ```

### Post Visibility

- Posts are automatically sorted by date (newest first)
- Only the 5 most recent posts appear on the home page
- All posts are visible on the `/blog` page

## Updating Experience

Edit the `_data/experience.yml` file to add or modify work experience entries:

```yaml
- company: Company Name
  role: Your Role
  period: Start Date – End Date
  location: City, Country
  description: Brief description of your work (optional)
```

## Structure

```
.
├── _config.yml           # Site configuration
├── _data/
│   └── experience.yml    # Work experience data
├── _layouts/
│   ├── default.html      # Base layout
│   └── post.html         # Blog post layout
├── _posts/               # Blog posts (Markdown files)
├── assets/
│   ├── css/
│   │   └── style.css     # Main stylesheet
│   └── images/           # Images for posts
├── index.html            # Home page
├── blog.html             # Blog listing page
├── Gemfile               # Ruby dependencies
└── README.md             # This file
```

## Features

- ✅ Clean, minimal design
- ✅ Responsive layout
- ✅ Dark/light mode (follows system preference)
- ✅ Blog with Markdown support
- ✅ Experience section from data file
- ✅ Fast load times (no heavy JavaScript)

## GitHub Pages Setup

This site is automatically deployed by GitHub Pages. To enable it:

1. Go to your repository settings
2. Navigate to **Pages** (under "Code and automation")
3. Under "Build and deployment":
   - **Source**: Deploy from a branch
   - **Branch**: `main` / (root)
4. Save the settings

GitHub Pages will automatically rebuild the site whenever you push changes to the `main` branch.

## License

This site and its content are personal property of Jimmy Akl.
