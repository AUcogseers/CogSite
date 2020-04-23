---
type: docs                  # Set the page type to blog or something else if it's outside the docs
weight: 1                   # This decides the page position in the menu compared to files in the same directory
# bookFlatSection: true     # Decides if it is a sections (bold font) in the menu
# bookCollapseSection: true # Creates a collapsing section (like the list of everything)
# bookHidden: true          # Hide this page in the left menu
# bookToC: false            # Hide the table of contents when on this page
# bookComments: false       # Disable comments (not super sure about the function of comments a.t.m.)
title: "Page settings"  # This is the page title
---

# Page settings

The page settings are present in the top of the .md (markdown) documents and are not rendered but are used to define how they are shown in the table of contents. For example, this is the current page's page settings in the top of the document:
```
title: "Page settings"
type: docs
weight: 1
```

You do not need the page settings on every page as they default to the file name and first heading of the page but if you want, here is a description of the possible page settings:

- type: docs
  - Set the page type to blog or something else if it's outside the docs
- weight: 1
  - This decides the page position in the menu compared to files in the same directory
- bookFlatSection: true
  - Decides if it is a sections (bold font) in the menu
- bookCollapseSection: true
  - Creates a collapsing section (like the list of everything)
- bookHidden: true
  - Hide this page in the left menu
- bookToC: false
  - Hide the table of contents when on this page
- bookComments: false
  - Disable comments (not super sure about the function of comments a.t.m.)
- title: "PAGE SETTINGS"
  - This is the page title
