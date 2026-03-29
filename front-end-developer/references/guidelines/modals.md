# Modals & Dialogs

Modals are used for focused tasks, confirmations, or critical actions.

------------------------------------------------------------------------

## Structure

``` html
<div class="modal">

  <div class="modal-header">
    <h2 class="modal-title">Title</h2>
    <button class="modal-close" aria-label="Close"></button>
  </div>

  <div class="modal-body">
    <!-- Content -->
  </div>

  <div class="modal-footer">
    <button class="btn-secondary">Cancel</button>
    <button class="btn-primary">Confirm</button>
  </div>

</div>
```

------------------------------------------------------------------------

## Guidelines

-   Header: clear title + close button
-   Body: short, focused content
-   Footer: Cancel (left) + primary action (right)
-   Use danger style for destructive actions

------------------------------------------------------------------------

## Rules

-   Use for short tasks only
-   Avoid multi-step workflows
-   Always allow closing

------------------------------------------------------------------------

## Close Behavior

-   Close button
-   Cancel action
-   Optional: click outside

------------------------------------------------------------------------

## Actions

-   Use: Save, Confirm, Delete, Cancel
-   Avoid vague labels like "OK"

------------------------------------------------------------------------

## Sizes

-   Small: confirmations
-   Medium: forms
-   Large: complex content (use sparingly)

------------------------------------------------------------------------

## Example: Delete Modal

``` html
<div class="modal">

  <div class="modal-header">
    <h2 class="modal-title">Are you sure?</h2>
    <button class="modal-close" aria-label="Close"></button>
  </div>

  <div class="modal-body">
    <p>
      If you continue, <strong>Item #1864</strong> will be permanently deleted.
    </p>
  </div>

  <div class="modal-footer">
    <button class="btn-secondary">Cancel</button>
    <button class="btn-danger">Yes, delete item</button>
  </div>

</div>
```
