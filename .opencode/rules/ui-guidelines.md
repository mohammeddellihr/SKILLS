# UI Guidelines

## No emojis

Do not use emojis in user interface elements.

```html
<!-- Bad -->
<button>Save 📁</button>
<label>Name 🏷️</label>

<!-- Good -->
<button>Save</button>
<label>Name</label>
```


## Color usage

Use colors sparingly and consistently. Colors should communicate meaning and intent, not decorate.

#### Primary

Used for main actions and brand elements.

Examples:

- Create button
- Submit button
- Save button
- Continue button
- Primary navigation actions

#### Secondary

Used for less important or alternative actions.

Examples:

- Back button
- Secondary navigation
- Optional actions

#### Info

Used for neutral informational messages.

Examples:

- System messages
- Notifications
- Informational alerts

#### Danger

Used for destructive or critical actions.

Examples:

- Delete button
- Irreversible actions
- Critical error alerts

#### Success

Used for positive confirmations and successful operations.

Examples:

- Success alert: User created successfully.
- Success alert: User updated successfully.
- Success alert: User deleted successfully.

## Breadcrumb

### Responsive Button Pattern

Action buttons inside breadcrumbs should display icon + text on desktop and icon-only on mobile to conserve space.

The text label must be hidden on small screens using responsive utility classes.

#### Behavior

| Screen Size | Display |
|-------------|---------|
| Mobile / Tablet (sm and below) | Icon only |
| Desktop (md and above) | Icon + text |

#### Example

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