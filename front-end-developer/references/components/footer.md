# Footer

The bottom section of a page or site. It closes the visual flow and provides secondary navigation or legal information.

## Structure
- Main Content (Optional: links, newsletter signup, contact info)
- Legal Content (Copyright, Terms, Privacy)

## Context-Specific Examples

### Application / Dashboard Footer Implementation
Often minimal within the application itself to maximize screen real estate for the main content. For our dashboard and web applications, the footer must follow this exact HTML structure:

#### Full Example Structure
```html
<footer class="footer mt-auto py-3 bg-light">
  <div class="container text-center">
    <span class="text-muted">
      <span id="current_year">2024</span> © App Name. All rights reserved.
    </span>
  </div>
</footer>
```

#### Key Rules:
- **Responsive Wrapper**: Use `<footer class="footer mt-auto py-3 bg-light">` to push the footer to the bottom of the page and apply appropriate padding and background color.
- **Container**: Wrap contents in `<div class="container text-center">` to center the text and limit width.
- **Dynamic Year**: Use `<span id="current_year">2024</span>` so the year can be dynamically updated via JavaScript.
- **Text Styling**: Wrap the text content in `<span class="text-muted">` for a subtle appearance.

### Marketing / Landing Page Footer
Typically larger ("Fat Footer") containing multiple columns of information.
- **Content**: 
  - Brand summary
  - Columns of links (Product, Company, Resources)
  - Social media icons
  - Newsletter subscription form
  - Copyright line