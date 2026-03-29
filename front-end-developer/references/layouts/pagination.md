# Pagination

The Pagination component provides navigation controls for lists and tables, typically residing in the footer of a data card.

## Responsive Button Pattern

Pagination relies heavily on the **Responsive Button Pattern** to ensure usability on mobile devices without breaking the layout. The core idea is to render *two* versions of the same button and use responsive display utilities (`d-sm-none`, `d-none`, `d-sm-inline-block`) to toggle between them.

## Structure

```html
<div class="card-footer">
  <div class="d-flex justify-content-between">
    
    <!-- Previous Button Group -->
    <div>
      <div class="btn-list">
        <!-- Mobile: Icon Only -->
        <a class="btn btn-primary disabled d-sm-none btn-icon" href="#">
          <svg>... (Left Arrow Icon) ...</svg>
        </a>
        <!-- Desktop: Icon + Text -->
        <a class="btn btn-primary disabled d-none d-sm-inline-block" href="#">
          <svg>... (Left Arrow Icon) ...</svg>
          Previous
        </a>
      </div>
    </div>
    
    <!-- Next Button Group -->
    <div>
      <div class="btn-list">
        <!-- Mobile: Icon Only -->
        <a class="btn btn-primary d-sm-none btn-icon" href="/profiles/?page=2">
          <svg>... (Right Arrow Icon) ...</svg>
        </a>
        <!-- Desktop: Icon + Text -->
        <a class="btn btn-primary d-none d-sm-inline-block" href="/profiles/?page=2">
          <svg>... (Right Arrow Icon) ...</svg>
          Next
        </a>
      </div>
    </div>
    
  </div>
</div>
```

## Guidelines

- **Container**: Place pagination inside a `.card-footer`.
- **Alignment**: Use `.d-flex.justify-content-between` to push the "Previous" controls to the left and "Next" controls to the right.
- **Responsive Duplication**: Always provide the `<a class="... d-sm-none btn-icon">` for mobile and `<a class="... d-none d-sm-inline-block">` for desktop. Do not attempt to hide text nodes with CSS alone; duplicate the button structure for bulletproof layout behavior.
- **Disabled State**: Apply the `disabled` class to the `<a>` tag when there is no previous or next page available.