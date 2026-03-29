# Data Grid

The Data Grid component is used to display read-only key-value data, typically on "View" or "Detail" pages. It aligns labels and values consistently.

## Structure

The core structure relies on a parent `.datagrid` container with `.datagrid-item` children. Each item contains a `.datagrid-title` (the label) and a `.datagrid-content` (the value).

```html
<div class="card-body">
  <div class="datagrid">
    <!-- Standard Item -->
    <div class="datagrid-item">
      <div class="datagrid-title">Public ID</div>
      <div class="datagrid-content">5783-7583-3878</div>
    </div>
    
    <!-- Item with link -->
    <div class="datagrid-item">
      <div class="datagrid-title">Appointment Name</div>
      <div class="datagrid-content">
        <a href="/appointments/4">NETHERLANDS | ALGIERS | TOURISM</a>
      </div>
    </div>
    
    <!-- Item with Status Badge -->
    <div class="datagrid-item">
      <div class="datagrid-title">Status</div>
      <div class="datagrid-content">
        <span class="status status-orange">
          <span class="status-dot"></span>
          In Progress
        </span>
      </div>
    </div>
    
    <!-- Full Width Item (e.g., for long notes) -->
    <div class="datagrid-item" style="grid-column: 1 / -1">
      <div class="datagrid-title">Note</div>
      <div class="datagrid-content">N/A</div>
    </div>
  </div>
</div>
```

## Guidelines

- **Container**: The `.datagrid` should typically live directly inside a `.card-body` or `.card-footer`.
- **Full Width Content**: For fields that contain a lot of text (like Notes, Descriptions, or JSON blobs), apply the inline style `style="grid-column: 1 / -1"` to the `.datagrid-item` so it spans all available columns.
- **Empty Values**: If a value is missing, explicitly render "N/A" or "Unavailable" (sometimes accompanied by an icon) to make it clear the field is not just broken.