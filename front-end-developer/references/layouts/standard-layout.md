# Standard Layout Structure

This defines the specific structural layout pattern used across our dashboard and web applications.

## High-Level Structure
- **Header / Sidebar**
  - Branding
  - NavigationSystem
    - NavigationItem
    - NavigationGroup (optional)
      - NavigationItem
  - UserSection
    - Avatar
    - UserMenu
      - Logout
  - MobileMenuToggle
- **Content Area**
  - PageHeader
    - Title
    - Subtitle
    - Actions
  - MainSection
    - ContentBlock (1 or more)
- **OverlayComponents** (Optional)
  - Modal / Drawers
- **Footer**
  - FooterContent (Minimal)

## Component Composition

### Layout Navigation
The navigation should be clear and hierarchically structured. Use `NavigationGroup`s to keep the menu from becoming too cluttered.

### Content Flow
1. Every page should begin with a `PageHeader` indicating exactly where the user is.
2. The core content lives within one or more `ContentBlock`s (cards) inside the `MainSection`.
3. Critical actions should be prominent in the `PageHeader`, while item-specific actions live within the `ContentBlock` (e.g., table rows).