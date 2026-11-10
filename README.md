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

## Content Management

### Adding a New Blog Post

Blog posts are written in Markdown and stored in the `_posts` directory.

#### File Naming Convention

Posts must follow this exact naming format:

```
YYYY-MM-DD-title-with-hyphens.md
```

**Examples**:
- `2024-11-10-my-first-post.md`
- `2024-12-25-christmas-thoughts.md`
- `2025-01-15-learning-rust.md`

#### Front Matter

Every post must start with YAML front matter between triple dashes:

```yaml
---
layout: post
title: "Your Post Title"
date: 2024-11-10
---
```

#### Full Example Post

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

#### Adding Images to Posts

1. Create an `assets/images` directory if it doesn't exist:
   ```bash
   mkdir -p assets/images
   ```

2. Add your image files to this directory

3. Reference them in your post:
   ```markdown
   ![Image description](/assets/images/my-image.png)
   ```

### Updating Experience

Edit the `_data/experience.yml` file to add or modify work experience entries:

```yaml
- company: Company Name
  role: Your Role
  period: Start Date – End Date
  location: City, Country
  description: Brief description of your work (optional)
  tags:
    - Technology
    - Skill
    - Domain
```

The `tags` field is optional and displays as colored pills on each experience card.

### Updating Education

Edit the `_data/education.yml` file to add or modify education entries:

```yaml
- institution: University Name
  degree: Degree Title
  period: Start Year–End Year
  location: City, Country
```

## Site Structure

```
.
├── _config.yml           # Site configuration
├── _data/
│   ├── experience.yml    # Work experience data
│   └── education.yml     # Education data
├── _layouts/
│   ├── default.html      # Base layout with sidebar
│   └── post.html         # Blog post layout
├── _posts/               # Blog posts (Markdown files)
├── assets/
│   ├── css/
│   │   └── style.css     # Main stylesheet
│   └── images/           # Images for posts (create as needed)
├── index.html            # Home page
├── blog.html             # Blog listing page
├── Gemfile               # Ruby dependencies
└── README.md             # This file
```

## Features

- ✅ Modern, standout design with sticky sidebar on desktop
- ✅ Refined typography using Inter font
- ✅ Accent color and polished dark mode
- ✅ Dark/light mode toggle (follows system preference by default)
- ✅ Fully responsive mobile layout
- ✅ Experience cards with tech/skill tags
- ✅ Blog with Markdown support
- ✅ Syntax highlighting for code blocks
- ✅ Hover states and smooth transitions
- ✅ Fast load times with minimal JavaScript

## Design Inspiration

The design draws inspiration from several standout developer portfolios:
- **brittanychiang.com** — Sticky sidebar layout
- **leerob.io** — Clean typography and minimal approach
- **joshwcomeau.com** — Polished dark mode and interactive elements
- **paco.me** — Typography and spacing refinement

## GitHub Pages Setup

This site is automatically deployed by GitHub Pages. To enable it:

1. Go to your repository settings
2. Navigate to **Pages** (under "Code and automation")
3. Under "Build and deployment":
   - **Source**: Deploy from a branch
   - **Branch**: `main` / (root)
4. Save the settings

GitHub Pages will automatically rebuild the site whenever you push changes to the `main` branch.

## Technical Details

- Built with Jekyll 3.x (via the `github-pages` gem for full compatibility)
- Uses Rouge for syntax highlighting
- Includes `jekyll-feed` and `jekyll-seo-tag` plugins
- Minimal vanilla JavaScript only for dark mode toggle
- No build tooling beyond Jekyll required
- All styles in a single CSS file for simplicity

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Responsive design tested at 320px minimum width
- Mobile-optimized with proper tap targets (44px minimum)

## License

This site and its content are personal property of Jimmy Akl.
