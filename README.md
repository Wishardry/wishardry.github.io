This is more for me and technical side of maintaining this blog posting stuff than an actual README. 

The entire site is made by Claude. 

## Quick notes:
informative → "Informative" tab
random → "Random" tab
shitposting → "The Corner" tab
llm → "LLM stuff" tab

# Blog Post Creation Guide for Wishardry's Red Room

## Quick Start Checklist
- [ ] Create markdown file with correct naming format
- [ ] Add proper YAML front matter
- [ ] Place file in `_posts/` directory
- [ ] Push to GitHub
- [ ] Wait 2-3 minutes for GitHub Pages to build

## File Naming and Location

### Naming Convention
Your blog post files must follow this exact format:
```
YYYY-MM-DD-Post-Title-With-Hyphens.md
```

**Examples:**
- `2025-07-29-My-First-Blog-Post.md`
- `2025-08-15-Understanding-LLM-Jailbreaking.md`
- `2025-12-25-Christmas-Thoughts.md`

### File Location
All blog posts go in the `_posts/` directory:
```
your-repo/
├── _posts/
│   ├── 2025-07-28-A-Conceptual-Understanding.md
│   ├── 2025-07-29-Your-New-Post.md
│   └── 2025-08-01-Another-Post.md
├── _config.yml
├── about.md
└── index.md
```

## YAML Front Matter

Every blog post must start with YAML front matter between triple dashes:

```yaml
---
layout: post
title: "Your Post Title Here"
date: 2025-07-29 14:30:00 -0500
categories: [category1, category2]
tags: [tag1, tag2, tag3]
excerpt: "A brief description of your post that appears in post cards"
---
```

### Front Matter Fields Explained

| Field | Required | Description | Example |
|-------|----------|-------------|---------|
| `layout` | ✅ Yes | Always use `post` | `post` |
| `title` | ✅ Yes | Post title (can have spaces, quotes recommended) | `"My Amazing Blog Post"` |
| `date` | ⚠️ Optional | Override the date from filename | `2025-07-29 14:30:00 -0500` |
| `categories` | ❌ No | Broad topic categories | `[red-teaming, ai-safety]` |
| `tags` | ❌ No | Specific keywords | `[jailbreaking, prompts, claude]` |
| `excerpt` | ❌ No | Custom excerpt for post cards | `"A deep dive into..."` |

## URL Structure

With your current permalink setting (`permalink: /:title/`), your URLs will be:
- **File**: `2025-07-29-Understanding-LLM-Prompts.md`
- **URL**: `https://wishardry.github.io/Understanding-LLM-Prompts/`

## Content Writing

### Basic Markdown
```markdown
# Main Heading (H1)
## Section Heading (H2)
### Subsection (H3)

**Bold text**
*Italic text*
`inline code`

[Link text](https://example.com)

> This is a blockquote
> for important notes

- Bullet point 1
- Bullet point 2
- Bullet point 3

1. Numbered item
2. Another item
3. Final item
```

### Code Blocks
````markdown
```python
def hello_world():
    print("Hello, Red Room!")
```
````

### Images
```markdown
![Alt text](/assets/images/my-image.png)
```

**Image Organization:**
- Place images in `/assets/images/`
- Use descriptive filenames: `prompt-injection-example.png`
- Keep file sizes reasonable (< 1MB for web)

## Publishing Workflow

### Method 1: GitHub Web Interface
1. Go to your repository on GitHub
2. Navigate to `_posts/` folder
3. Click "Add file" → "Create new file"
4. Name your file: `2025-07-29-My-Post-Title.md`
5. Add your content with front matter
6. Scroll down, add commit message
7. Click "Commit new file"

### Method 2: Local Development
1. Clone your repository
2. Create new file in `_posts/`
3. Write your post
4. Commit and push:
```bash
git add .
git commit -m "Add new blog post: Post Title"
git push origin main
```

### Method 3: Using Your Conversion Tool
1. Create your post content however you prefer
2. Use your conversion tool to format it properly
3. Save the output as `YYYY-MM-DD-Title.md` in `_posts/`
4. Push to GitHub

## Build and Deployment

### GitHub Pages Build Process
- **Trigger**: Any push to your main branch
- **Build Time**: 2-3 minutes typically
- **Status**: Check the "Actions" tab in your GitHub repo

### Troubleshooting Build Issues
If your site doesn't update:

1. **Check the Actions tab** for build errors
2. **Common issues:**
   - Missing front matter
   - Invalid YAML syntax
   - Incorrect file naming
   - Files not in `_posts/` directory

### Testing Locally (Optional)
If you want to preview posts before publishing:
```bash
# Install Jekyll
gem install bundler jekyll

# In your repo directory
bundle install
bundle exec jekyll serve

# Open http://localhost:4000
```

## Content Best Practices

### Writing Style
- **Headers**: Use descriptive headings for easy scanning
- **Paragraphs**: Keep them short (2-4 sentences)
- **Code**: Always use syntax highlighting
- **Links**: Use descriptive link text, not "click here"

### SEO-Friendly Posts
- Include your main keywords in the title
- Use headings (H2, H3) to structure content
- Write compelling excerpts
- Add relevant tags and categories

### Post Length
- **Short posts**: 500-800 words
- **Medium posts**: 800-1500 words  
- **Long-form**: 1500+ words

## File Organization Tips

### Folder Structure
```
_posts/
├── 2025-07-28-A-Conceptual-Understanding.md
├── 2025-07-29-LLM-Red-Teaming-Basics.md
├── 2025-08-01-Prompt-Injection-Examples.md
└── 2025-08-15-Advanced-Jailbreaking.md

assets/
├── images/
│   ├── prompt-example-1.png
│   ├── jailbreak-demo.gif
│   └── red-team-diagram.jpg
└── main.scss
```

### Naming Conventions
- **Posts**: `YYYY-MM-DD-Title-With-Hyphens.md`
- **Images**: `descriptive-name.png/jpg/gif`
- **No spaces** in filenames
- **Use hyphens** instead of underscores

## Common Mistakes to Avoid

❌ **Wrong filename format**: `my-post.md` (missing date)
❌ **Missing front matter**: Starting directly with content
❌ **Wrong directory**: Putting posts in root instead of `_posts/`
❌ **Invalid YAML**: Forgetting quotes around titles with special characters
❌ **Large images**: Using multi-MB images that slow load times

## Your Current Theme Features

### Styling Elements Available
- **Post cards**: Automatic with title/date layout
- **Dark/light mode**: Theme toggle in header
- **Responsive design**: Mobile-friendly layouts
- **Typography**: Source Serif 4 for readability
- **Code highlighting**: Syntax highlighting enabled

### Special Features
- **Clean URLs**: No dates in post URLs
- **Load more**: Pagination on homepage (8 posts initially)
- **Excerpts**: Automatic or custom post previews
- **Warm color scheme**: Red/coral theme matching your brand

## Quick Reference

### Minimal Blog Post Template
```markdown
---
layout: post
title: "Your Post Title"
---

Your content starts here.

## A Section Header

Write your thoughts, share your insights, and engage your readers.

```

### Full Blog Post Template
```markdown
---
layout: post
title: "Complete Guide to Something Important"
date: 2025-07-29 15:00:00 -0500
categories: [guides, technical]
tags: [tutorial, step-by-step, beginner-friendly]
excerpt: "Learn everything you need to know about this important topic in this comprehensive guide."
---

# Introduction

Brief overview of what this post covers.

## Main Content Section

Your detailed content here.

### Subsection

More specific details.

## Conclusion

Wrap up your thoughts and next steps.

```

## Getting Help

If something isn't working:
1. Check GitHub Actions for build errors
2. Verify your file is named correctly
3. Confirm YAML front matter syntax
4. Make sure file is in `_posts/` directory
5. Wait 2-3 minutes after pushing for changes to appear

Your blog setup is designed to be simple - focus on writing great content, and the technical aspects should just work!
