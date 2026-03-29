---
name: ui-structure
description: Define UI structure patterns for header, content, overlay, and footer components
---

# UI Structure

## Structure

- Header
  - Branding
  - NavigationSystem
    - NavigationItem
    - NavigationGroup (optional)
      - NavigationItem
  - UserSection (optional)
    - Avatar
    - UserMenu
      - Logout
  - MobileMenuToggle
- Content
  - PageHeader
    - Title
    - Subtitle
    - Actions
  - MainSection
    - ContentBlock
    - ContentBlock
- OverlayComponents (optional)
  - Modal
- Footer
  - FooterContent

## Examples

### Header

The top section of the page containing branding, navigation, user controls, and mobile menu toggle.

#### Branding

The logo or brand name that links to the home page. Example: "Acme Corp" logo or text.

#### NavigationSystem

Primary navigation container that holds NavigationItems and NavigationGroups.

#### NavigationItem

A single link in the navigation menu. Example: "Dashboard", "Settings", "Users".

#### NavigationGroup

A group of related NavigationItems that can be collapsed. Example: "Settings" group containing "Account", "Preferences", "Security".

#### UserSection

Optional section showing the current user info and actions.

#### Avatar

User profile image or initials. Example: User photo or "JD" for "John Doe".

#### UserMenu

Dropdown menu with user-related options. Example: "Profile", "Settings", "Logout".

#### MobileMenuToggle

Button to show/hide navigation on mobile devices.

### Content

The main area between Header and Footer containing PageHeader, MainSection.

#### PageHeader

Top section of content area with title, subtitle, and action buttons.

##### Title

The main heading of the current page. Example: "Dashboard", "Users", "Contacts".

##### Subtitle

Supporting text below the title. Example: "User #218", "Contact #58".

##### Actions

Buttons for primary actions available on a page.

Examples:

- Create (typically on list pages)
- Update (typically on entity view pages)
- Delete (typically on entity update pages)

#### MainSection

The primary content area displaying the main page content.

#### ContentBlock

ContentBlocks are always displayed as cards col-12.

Examples:

- User List
    - Header: No
    - Body: table
    - Footer: Previous/Next or Pagination
- User Create (header, body, footer)
    - Header: Create User
    - Body: form
    - Footer: Cancel button and Create User button
- User View (header, body, footer)
    - Header: View User
    - Body: Data Grid
    - Footer: Created and Updated

### OverlayComponents

Components that appear on top of the main content.

#### Modal

A dialog box that requires user interaction. Example: "Confirm Delete".

### Footer

The bottom section of the page.

#### FooterContent

Content at the bottom including copyright. Example: "2024 Company Name. All rights reserved.".
