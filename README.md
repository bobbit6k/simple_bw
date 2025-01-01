# Simple BW Theme Documentation

## Overview
Simple BW is a clean, minimalist theme for Zola static site generator. It features:

- Responsive design
- Customizable color scheme
- Modular components
- Built with SASS for easy styling

## Installation
1. Add the theme to your Zola project:
```toml
[theme]
name = "simple_bw"
```

2. Copy the theme files to your project's `themes/simple_bw` directory.

## Configuration
The theme can be configured through the `config.toml` file under the `[extra]` section. Available options:

```toml
[extra]
# Show/hide newsletter section
show_newsletter = true

# Show/hide breadcrumbs navigation
show_breadcrumbs = true

# Footer links configuration
footer_links = [
    {name = "Terms", url = "/terms"},
    {name = "Privacy Policy", url = "/privacy"},
    {name = "Manage cookies", url = "/cookies"}
]
```

## Components
The theme includes several reusable components:

### Header
Responsive navigation header with:
- Logo display (configured via `logo.png` in images directory)
- Mobile menu toggle
- Automatic navigation menu generation from sections/pages marked with `is_main_nav`
- Mobile menu overlay with:
  - Close button
  - Footer section containing contact and signup buttons

### Hero Section
Prominent hero section featuring:
- Profile image (configured via `roberto-berneri.webp` in images directory)
- Name and title display
- Two text sections: intro and description
- Highlighted text in description section
- Learn more call-to-action button

### Social Share
Open Graph meta tags for social media sharing with:
- Dynamic title and description based on page/section content
- Configurable Open Graph image through:
  - Page-specific `og_image`
  - Section-specific `og_image`
  - Default `og_image` in config

### Table of Contents
Collapsible table of contents with:
- Optional display controlled via `toc` flag in page/section extra
- Supports both section and page content
- Handles hierarchical headings (H1 and H2)
- Configurable introduction text via `config.extra.toc_intro`

### Extra Scripts
Additional JavaScript functionality including:
- Mobile menu toggle for non-homepage routes
- Menu overlay visibility control
- Body overflow management during menu open state
- Event handling for both menu opening and closing

## Customization
To customize the theme:

1. Edit the SASS files in `sass/`
2. Modify the HTML templates in `templates/`
3. Add custom styles in `static/css/`

## Usage
To use the theme in your content:

```markdown
+++
title = "My Page"
template = "page.html"
+++

Page content goes here
```

## License
MIT License
