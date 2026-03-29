# Header

The top section of the page, typically containing branding and primary navigation.

## Generic Structure
- Branding (Logo / Site Name)
- Navigation System (Primary links)
- Utility Section (Search, User actions, Settings)
- Mobile Menu Toggle (For responsive views)

## Standard Header Implementation
For all our applications (using Bootstrap / Tabler UI patterns), the header must follow this exact HTML structure:

#### Full Example Structure
```html
<header class="navbar navbar-expand-md navbar-light d-print-none">
  <div class="container-xl">
    
    <!-- Mobile Toggle -->
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbar-menu" aria-controls="navbar-menu" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    
    <!-- Branding -->
    <h1 class="navbar-brand navbar-brand-autodark d-none-navbar-horizontal pe-0 pe-md-3">
      <a href="/" style="text-decoration:none">
        App Name <span class="badge">v1.0.0</span>
      </a>
    </h1>
    
    <!-- User Section (Right aligned) -->
    <div class="navbar-nav flex-row order-md-last">
      <div class="nav-item dropdown">
        <a href="#" class="nav-link d-flex lh-1 text-reset p-0" data-bs-toggle="dropdown" aria-label="Open user menu">
          <span class="avatar avatar-0">
            <!-- Icon or Image -->
            <svg>...</svg>
          </span>
          <div class="d-none d-xl-block ps-2">
            <div>User Name</div>
            <div class="mt-1 small text-muted">user@example.com</div>
          </div>
        </a>
        <div class="dropdown-menu dropdown-menu-end dropdown-menu-arrow">
          <a href="/profile" class="dropdown-item">Profile</a>
          <a href="/settings" class="dropdown-item">Settings</a>
          <div class="dropdown-divider"></div>
          <a href="/logout/" class="dropdown-item text-danger">Logout</a>
        </div>
      </div>
    </div>
    
    <!-- Navigation Links -->
    <div class="collapse navbar-collapse" id="navbar-menu">
      <div class="d-flex flex-column flex-md-row flex-fill align-items-stretch align-items-md-center">
        <ul class="navbar-nav">
          <!-- Standard Link -->
          <li class="nav-item">
            <a class="nav-link" href="/users/">
              <span class="nav-link-title">Users</span>
            </a>
          </li>
          
          <!-- Dropdown Menu (Manage) -->
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#navbar-extra" data-bs-toggle="dropdown" data-bs-auto-close="outside" role="button" aria-expanded="false">
              <span class="nav-link-title">Manage</span>
            </a>
            <div class="dropdown-menu">
              <a class="dropdown-item" href="/appointments/">Appointments</a>
              <a class="dropdown-item" href="/nationalities/">Nationalities</a>
            </div>
          </li>
        </ul>
      </div>
    </div>
    
  </div>
</header>
```

#### Key Rules:
- **Responsive Wrapper**: Use `<header class="navbar navbar-expand-md navbar-light d-print-none">` to ensure it hides during printing and collapses properly on mobile.
- **Container**: Wrap contents in `<div class="container-xl">`.
- **User Dropdown**: Always place `navbar-nav flex-row order-md-last` so the user menu stays on the right and remains visible or easily accessible on mobile. Avatar + Name/Email (hidden on small screens using `d-none d-xl-block`).
- **Logout Action**: Ensure the logout button is visually distinct using `.text-danger`.
- **Navigation Links**: Wrap links in `.navbar-collapse` targeting `#navbar-menu`. Menu items use `.nav-item` and `.nav-link`, with text inside `<span class="nav-link-title">`.
