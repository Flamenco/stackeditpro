Here is *what's new* in this edition of **StackEditPro**.

# New Features

## Workspace Search
We have enabled text searching of all documents inside your workspace.
You can search by file name and/or content.  There is also and option to specify case-sensitivity.

Search results are ordered by *most recently used (MRU)*.

The search is available from the *main toolbar*, the *main menu*, and the *explorer toolbar*.
Pressing on the search action will toggle the search dialog visibility.

A preview option in the search results list is available to open the document in the background while keeping the search results window open.

## Filter The Navigator Files/Folder Tree
You can now filter the navigator tree by name.  The search uses a *contains* filter and is *case insensitive*.
You can continue to edit and create new items while the tree is filtered.  A clear button allows quickly resetting your search.

## Sharing
We added support for sharing.  You can share a workspace, a folder, or a file with a single click.
The navigator now shows an icon if a file or folder is shared directly or indirectly.

Sharing can be configured from the *Main Menu / Sharing Menu* or from the *File Info* page.

Your sharing settings will synchronize between workspaces.

See [Sharing](Sharing.md).

## TOC More Accessible
The Table Of Contents command gets used the most, so we moved it to the top of the sidebar menu.

We also added a shortcut to open/close the *Table of Contents* to the Navigation Bar.

###  Auto Close Table Of Contents On Narrow Device
If the Table Of Contents is in fullscreen mode, it will close when selecting a topic.  This makes navigating your documents a breeze.

## Workspace Links
You can now add links to workspace documents and folders from other documents.  We added an additional field to the `Add Links` action in the toolbar.

Links use the document or folder id;  Renaming or moving a document will not break the link. 

## Navigation
You can now navigate your workspace by either visited history or natural document order.

### Arrow Navigation
*Previous Document* and *Next Document* links have been added to the Navigation Bar.  This allows you to navigate within your document tree using *natural document order*.

### History Mode
You can now use the browser's forward and back buttons to revisit your document and folder navigation sequence.

## Bookmarkable URLs
Your current document is now stored in the URL.  You can easy create bookmarks to a specific document or folder.

## Implemented *Empty Trash*
We fixed logic that prevented un-synced workspaces from emptying trash, and added an **Empty Now** action.  You can find this action in the _More... Menu_, and the *Folder Details View* when the `trash` folder is selected.

## Language Support
We have added support for setting a default language.  You can access the language select via the *Main Menu* `set language` or  via the *Global Action Menu* `sidebar : actions : set language`

Languages are stored as a browser setting, not a workspace setting.

> Not all forms and menus have been translated yet.

## Task And TODO search
Search your workspace for markdown task items and  `~todo~` blocks.

```
- [ ] Water Plants
- [ ] Feed Dogs
- [x] Walk Dogs

~todo Take out the trash.~
```

A report with all of your uncompleted tasks and todo items will open.
You can click a link to open the document that contains the item.

## New Markdown Extensions

### Copy-Code-Fence-To-Clipboard Extension
You can now press a button to copy code fence source code to your clipboard.

A *Copy Source Code* will appear at the top-left of your rendered fences.

> If you have defined a caption using the *Code-Fence-Caption Extension*, it will be removed from copied source code.e ocumentation 

### Code-Fence-Caption Extension
We extended the code fence syntax by adding a *caption syntax*.  If the first line of your fence starts with text between brackets `[Like This]`, it will be pulled out of the fence content, and added as a caption.  `Copy to Clipboard` will not include the caption block.

```
[My Title]
line 1
line 2
```

### Page-Title Extension

We added a syntax for adding titles to your pages without needing to use a heading. This results in the having a nice page name that does not get added in your heading or table of contents. It also allows for a separate *page-title* CSS style.

Page titles add a nice look to your documents, especially when using the navigation arrows to read across multiple pages.

You specify a title as your first line using text between `[` and `]`, followed by a blank line.
```
[My Great Page] 

# Part 1
# Part 2
```
You can also dynamically use the actual page name by declaring  `[]` as your first line, followed by a blank line.
```
[] 

# Part 1
# Part 2
```

Finally, you can add page titles to all your pages by setting a global property under `settings`.
```yml
pro:
 pageTitle:
  showAll: true
```

If you do not explicitly specify a page name, and the page is README, the parent folder is added to the rendered title.

### Source-Code-Documentation-Extension

Document source code outside of your codebase and render it as beautiful HTML.

See [Source Code Documentation Extension](Source%20Code%20Documentation%20Extension.md).

## Folder Overview
We now display a folder overview, shown when a folder is selected in the navigator.
You can view the folder contents by name or accessed date.

If there are items in the trash folder, and the trash folder is selected, an *Empty Trash Now* button will be enabled.

Columns are sortable by *name* or *last modified*.

Each item has a list of actions that can be performed.  You can hide or filter actions using the filters located at the top of the overview.

## Actions Menu
We added an *Actions Menu* to the *Main Menu*.  The actions menu lists all global and item actions added by the system and 3rd party plugins.

The folder actions list can be filtered by action name.

See [Actions](Actions.md).

## Recent Activity
View and activate documents based on a *most recently modified* list.
This action opens a dialog, and is available in the main toolbar.

## Browser Tab Title
The browser-tab title now displays the name of the current document.  It also allows your page name to appear in your search history and title bar.

## Workspace Name In Status Bar
The name of your current workspace is now displayed in the status bar at the bottom of the editor or viewer.

## More Programming Languages Added
We added additional languages to your code fences.

## Workspace Information Added
We added a section to the *More Sidebar* that displays workspace information, including folder and file counts,  workspace synchronization details, network connectivity, and more.

## StackEditPro CloudServices Login
You can now login to StackEditPro CloudServices, even if you have not linked a workspace.

## Email Documents
You can now email document content and links.  You must have a verified account email address to access this feature.

## Document Refactoring
### Extract Selection To New Document
You can now select any text in one document and create a new sibling document from it.

This procedure is equivalent to:
* Cutting the selected code
* Creating a new document using the selected code's heading for a name
* Pasting the code into the new document
* Adding a heading and page link to the original document.

> You will be presented with an *Extract Text confirmation dialog* when executing this action.  This dialog allows you to specify the new name if different than the first heading of the selection.

# Fixes
## IOS
### Cut, Copy, Paste, and Select - Fixed On iOS
In the original StackEdit, you cannot cut, copy, or paste in the Markdown editor while using iOS.  This is a total PITA, and quite frankly, a dealbreaker.  Alas, now It works.

### Unwanted Blank Lines and Tab Removal When Pasting
When pasting terminal code from OSX, extra lines were added to each line, and the tabs were removed.  That is now fixed.

### iOS Momentum Scrolling
Momentum scrolling has been enabled (fixed) for iOS devices.

## Fixed Google Login Profile Retrieval
Your name will now be displayed in the *Signed In As* section, and the *"Log into Google+..."* message will now stop showing up every time you visit the site.

## Synchronization Triggers
When you enter or exit edit mode, a sync is performed.  This eliminates the need to *merge*, and prevents duplicate information getting appended or removed from documents.

## Synchronization Logging
When a document has changed and is merged, a log item is created.  This item shows the client, server, and merged versions of the content.

## iOS Momentum Scrolling
Momentum scrolling has been enabled (fixed) for iOS devices.

## Selectable Root Node
There was no way to select the root node in the explorer.  This made it difficult to add a file or folder on the top level.

## GitLab Commit URL fixed
A setting that resulted in 500 http status was patched.

## Default Line Break Behavior
In Markdown, unless a single line break is followed by 2 spaces, it should not be considered a new paragraph.  And when followed by 2 spaces, it should be a line break in the same paragraph.

Both the *GitHub Flavored Markdown (GFM) Preset* and the *Default Preset* did not respect this, so we fixed it.

If you want the non-conventional behavior, create your own preset or override in you document settings.  You probably won't want the older behavior though...

## Async Markdown Extensions
There was no way for an markdown extension to run asynchronously.
This was an issue when rendering in the background, creating dynamically updating pages, or when exporting.  We added semantics to make this happen.

This feature also opens the door to Canvas-To-JPEG conversions for exports.

## CSS Injection For Extensions
Extensions can now inject custom CSS into exported documents.  We automatically export code fence CSS too, so your exported source code is styled.

## Default Table Alignment Property
Tables will now vertically align their cell content to the top.

## Blank Default Document
The default *New Document* is now blank. No more shameless self promotion for us.  No more having to cut crap from every new document for you.

## Sponsor Links Removed
It's all free now.  Well, almost free.  After our beta period we will be charging $.01 a month for each file you sync beyond a TBD quota.  We have removed all _monetize_ links and sponsor related network activity.

## Landing Page Removed
The default landing page now takes you right into the editor.  No more shameless self promotion.  We would rather make our app more useful for existing users, versus trying to ring in new users.


# Internal Changes

See [Internal Changes](Internal%20Changes.md).

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTY4NjYxMDI2MSwtMTE3Mzg3MDI0MiwxMD
c5MTM3MTIsLTgxNjI4NDgwNCwtMTE0MDYwMTQ4NSwtMTA5NTYx
Mjg3NCwxOTg5MzE2MDY3LDg1MDg0MjE1NCwtOTAyNjY1NDc1LC
0xOTc0MjYwNzY0LC03MTY2OTQyMSwyMDA4NDk5OTA5LDEyMjUx
NTUyNTAsMTIyNjI3OTcwNyw1NTM4NTU4NDAsNTk3MTk3Njk2LC
0xMTExMTA4MTk0LDExMzk2MzAxMTAsMTYxNDcwMTIxMiwxODA3
MDI2ODAxXX0=
-->