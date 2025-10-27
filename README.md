# My Books Blog

An Eleventy-powered website for previewing my fiction books.

## Features

- Homepage with all books displayed in a card grid
- Individual book pages with chapter listings
- Chapter preview pages with navigation
- Markdown-based chapter content
- Responsive design
- Clean, modern styling

## Books Included

1. **Rejacked** - A cyberpunk thriller
2. **Binary Heart** - AI and consciousness exploration
3. **RoboCop** - Justice and humanity reimagined

## Getting Started

### Install Dependencies

```bash
npm install
```

## Customization

### Adding New Books

1. **Create a book folder** in `src/books-content/` (e.g., `my-new-book`)
2. **Add chapter markdown files** (e.g., `chapter-01.md`, `chapter-02.md`)
3. **Create a book page** in `src/books/my-new-book.njk`:

```yaml
---
layout: book.njk
bookId: my-new-book
title: My New Book
description: An exciting new story
permalink: /books/my-new-book/index.html
---
```

4. **Add to books.json** in `src/_data/books.json`:

```json
{
  "id": "my-new-book",
  "title": "My New Book",
  "description": "An exciting new story"
}
```

That's it! No JavaScript required.

### Writing Chapters

Each chapter markdown file uses frontmatter and markdown content:

```markdown
---
layout: chapter.njk
bookId: my-new-book
bookTitle: My New Book
chapterNumber: 1
title: Chapter Title
permalink: /books/my-new-book/chapter-1/index.html
tags: chapters
---

Your chapter content goes here. Use standard markdown formatting:

**Bold text**, *italic text*, and regular paragraphs.

New paragraphs are separated by blank lines.
```

- Frontmatter defines metadata (between `---` markers)
- Content is written in standard markdown below frontmatter
- Eleventy automatically renders markdown to HTML

### Styling

Edit `src/css/style.css` to customize colors, fonts, and layout.

### Templates

- Modify `src/_includes/base.njk` to change the overall page structure
- Edit `src/_includes/book.njk` for book detail page layout
- Edit `src/_includes/chapter.njk` for chapter page layout

## Technologies Used

- [Eleventy](https://www.11ty.dev/) - Static site generator
- Nunjucks - Templating engine
- Markdown - Content format (built into Eleventy)
- CSS - Styling

## Key Features of This Setup

✅ **Minimal JavaScript** - No custom data processing scripts
✅ **Simple Configuration** - Just 12 lines in `eleventy.config.js`
✅ **Frontmatter-based** - Chapter metadata lives with the content
✅ **Collections-powered** - Uses Eleventy's built-in collections
✅ **Easy to edit** - Just edit markdown files to update content
