# Data Corruption
There is an ongoing dActive Issues
* Data corruption when merging data between 3+ clients.  The core sync engine incorrectly senses that files need to be merged, and odd remnants appear. 

When a merge happens, we add a *Merge Conflict Report* document to your workspace to indicate what was merged and when it happened.  You can then view the history of your document if you need to fix it.  The merge report also includes the pre and post merge versions for your convenience.

In our experience, most situations that require a merge really needed the server version.  An the default merge operation resulted in a corrupt document.  We decided that when it is detected that the servand client changed, we will keep the server, and create a report with all 3 versions (client, server, and merge).

# Move File Dialog
The window in not tall enough.  It should size to full screen.  Use a filtered choice picker.

# iOS Resize
The application does not respond to orientation changes well.

# Source Code Documentation Extension
~~Parameter descriptions are not implemented for Typescript interface methods.~~

# Zendesk Publishing Not Implemented
Send us an email if you require Zendesk support.

# Sharing
The sharing server does not render mermaid, fences, or other canvas-based extensions.

# Feature Requests
* Add scrolling divs (or toolbar popup) to toolbar.  Tools are not available on a narrow device.
* Export canvas as png.
* Create plugin architecture.
* Tasks
	* Complete task from task report.
	* Integrate tasks with external systems.
	* Scroll to line when selecting search and task links.
* Document driven design integration.


## Workspaces
* Grav
* StackEditPro
## Publish
* Blogger
* Dropbox
* GitHub
* GitLab
* Google Drive
* Wordpress
* Zendesk
* Grav
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1OTAzMzQwOTksMTU0MzM4NTQ5OSwtOT
Q3MTEwODIyLC0zMDQ0MTk1NzAsMjA5OTA0MTM0NiwxNjM4MDIx
MTQ3LDE3NTgzNDM2OTcsLTIwODMyMDAwMTMsLTE0MTY1MzMxMz
MsNjU1ODUwNTE1LDEwNDI5Mzc1MjUsMTcyMzcwNDEwMSwyNTk5
NzAzNDYsLTE4MDAxNzMwOTYsNjU1ODUwNTE1LC01MzE0MDE1OD
EsLTI0NTg1OTA1LC0xMzI3MzEzMTIyLC0xOTU3OTE4NTc3LDc4
NjczMTg4OV19
-->