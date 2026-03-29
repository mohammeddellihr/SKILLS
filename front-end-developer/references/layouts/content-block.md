# Content Block

Content blocks (or cards) group related information within the main content area. They provide visual separation and structure to the data.

## Structure
- Header (Optional)
- Body (Required)
- Footer (Optional)

## Guidelines
- Use cards or panels for content blocks to ensure consistent padding and background separation.
- Blocks should typically be responsive and scale to full width (`col-12`) on mobile.

## Common Configurations

### Data List
- **Header**: Not required if the Page Header already describes the list.
- **Body**: Table or list of items.
- **Footer**: Pagination controls.

### Form / Create View
- **Header**: E.g., "Create User" or "New Post"
- **Body**: Form fields logically grouped.
- **Footer**: Cancel button (left) and Submit button (right).

### Detail / Data View
- **Header**: Title of the entity being viewed.
- **Body**: Use the [Data Grid](data-grid.md) component (`.datagrid`) for displaying read-only key-value pairs.
- **Footer**: Metadata (e.g., "Created at: ...", "Last updated: ...") in a datagrid layout.

## Related Lists

On Detail/View pages, when an entity has related sub-collections (e.g., a Profile has many Applicants), stack them below the main Detail Content Block using the following structure:

```html
<!-- Separator Title -->
<div class="col-12">
  <h2 class="page-title">Related Items (Count)</h2>
</div>

<!-- Related List Card -->
<div class="col-12">
  <div class="card">
    <div class="table-responsive">
      <table class="table table-vcenter table-nowrap card-table">
        <!-- Table Content -->
      </table>
    </div>
  </div>
</div>
```