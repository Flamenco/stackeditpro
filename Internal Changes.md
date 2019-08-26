# Internal Changes

## All Software Updated To Latest Versions
Node on the backend now uses `NodeJS 12`.
All `npm` packages are now current, too.
* Babel was upgraded from 6.x to 7.x
* Mermaid now uses 8.1.0.

## Typescript Support
We have started converting the entire application to Typescript.

## Refactored Backend
All server-based services that operate on documents have been moved to a separate backend service.  For development, this facilitates a better developer workflow.  For deployment, it offers higher availability and improved scaling.

## i18n Support
We added internal support for internationalization.

### Removed AWS And Added MongoDB
The backend code that managed user data was changed from Amazon to a self hosted MongoDB instance.

## Refactored Front End
Removing the backend services made the front-end Docker image 4GB smaller.

## i18n Support
We added support for internationalization.

## Reworked Modal Dialogs
Modal Dialogs look and behave better.  They now will always scroll to top when opened.  The close buttons no longer scroll out of view.

We also added the ability to specify buttons when invoking a dialog.

## Jentify Integration
We have added the **Jentify Runtime Overlay** to help manage the growing complexity of the application model and UI.  This separates the actions from the UI, unifies dialogs, and provides a CLI.

## Jentify Security Integration
We added the Jentify Security Module to manage logins, authentication, and authorization.

## StackEdit 4 Support Removed
We no longer support StackEdit 4 and the overhead that accompanied it. 

## Recently Modified
There is was no *last-modified* data associated with files, so we could not sort and filter by that field.  We added a synced data object that now contains when, by whom, the device, and geo-location the modification was made.

## StackEditPro User ID
We added the ability to link multiple workspaces to a single user ID.

## Babel Prism Plugin
We removed the Gulp Prism script and replaced it with the Babel Prism Plugin.  We updated the default languages to include *Go* and *Typescript*.

## Allow other input types for FormEntry
The default forms would only allow input and select elements inside.

## Ecosystem And Culture
We get things done here.  Quickly and without ego.  We encourage feature and bug requests. We will not leave issues without responses for weeks, months, or years as seen in other projects.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc0MDkwMTMzMywtMTM0NDAyMzgzOSwxNz
MxMDc3NCwtMjM3MzkxNDU3LDc5MzEwODM4OV19
-->