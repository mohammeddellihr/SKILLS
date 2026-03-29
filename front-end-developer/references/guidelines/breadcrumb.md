# Breadcrumb

## Responsive Button Pattern

Action buttons inside breadcrumbs should display icon + text on desktop and icon-only on mobile to conserve space.

The text label must be hidden on small screens using responsive utility classes.

### Behavior

| Screen Size | Display |
|-------------|---------|
| Mobile / Tablet (sm and below) | Icon only |
| Desktop (md and above) | Icon + text |

### Example

```html
<!-- Action Button -->
<a href="/users/create" class="btn btn-primary">
  <!-- icon -->
  <svg xmlns="http://www.w3.org/2000/svg"
    width="24"
    height="24"
    fill="none"
    stroke="currentColor"
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    class="me-sm-1"
    viewBox="0 0 24 24">
    <line x1="12" y1="5" x2="12" y2="19"></line>
    <line x1="5" y1="12" x2="19" y2="12"></line>
  </svg>
  <!-- text hidden on mobile -->
  <span class="d-none d-sm-inline">Create Profile</span>
</a>
```