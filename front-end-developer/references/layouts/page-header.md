# Page Header

The top section of a content area that introduces the context of the page.

## Structure
- Pre-title (Breadcrumb / Parent link)
- Title
- Actions (Responsive Button Pattern)
- Filters (Dropdown, Optional)

## Guidelines
- **Pre-title**: A small link above the title (`.page-pretitle`) acting as a back-link to the parent list.
- **Title**: The main heading (`h2.page-title`) of the current page. Keep it concise.
- **Actions & Filters**: Placed in a `.col-auto.ms-auto` container using a `.btn-list` wrapper.

### Responsive Button Pattern
Every action button in the header **MUST** implement the responsive duplication pattern:
1.  **Mobile Version**: Icon-only button (`d-sm-none btn-icon`)
2.  **Desktop Version**: Icon + Text button (`d-none d-sm-inline-block`)

This ensures the layout doesn't break on small screens while remaining accessible.

## Examples

### List View with Filter and Create Action
```html
<div class="page-header" style="margin:0">
  <div class="row align-items-center">
    <!-- Title Area -->
    <div class="col">
      <div class="page-pretitle">
        <a href="/" style="color:#6b7280;text-decoration:none">Dashboard</a>
      </div>
      <h2 class="page-title">Profiles</h2>
    </div>
    
    <!-- Actions Area -->
    <div class="col-auto ms-auto">
      <div class="btn-list">
        
        <!-- Filter Dropdown -->
        <div class="dropdown">
          <!-- Mobile Filter Button -->
          <a class="btn d-sm-none btn-icon" href="#" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
            <svg>... (Filter Icon) ...</svg>
          </a>
          <!-- Desktop Filter Button -->
          <a class="btn d-none d-sm-inline-block" href="#" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
            <svg>... (Filter Icon) ...</svg> Filter
          </a>
          <div class="dropdown-menu dropdown-menu-end">
            <span class="dropdown-header">Status</span>
            <a class="dropdown-item" href="?status=active">Active</a>
          </div>
        </div>

        <!-- Create Button -->
        <!-- Mobile Create -->
        <a class="btn btn-primary d-sm-none btn-icon" href="/profiles/create">
          <svg>... (Plus Icon) ...</svg>
        </a>
        <!-- Desktop Create -->
        <a class="btn btn-primary d-none d-sm-inline-block" href="/profiles/create">
          <svg>... (Plus Icon) ...</svg> Create Profile
        </a>
        
      </div>
    </div>
  </div>
</div>
```

### Detail View with Multiple Actions
- Title: "John Doe"
- Actions:
  - Create Related Entity (Secondary)
  - Edit Profile (Primary)
- Note: Destructive actions like "Delete" belong in the page header of the **Update/Edit** page, not typically the View page.