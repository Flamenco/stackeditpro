# Data Corruption
There is an ongoing data corruption when merging data between 3+ clients and a server.  The core sync engine incorrectly senses that files need to be merged, and odd remnants appear. 

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

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg0OTI2NjA4MiwxNTQzMzg1NDk5LC0xNT
kwMzM0MDk5LDE1NDMzODU0OTksLTk0NzExMDgyMiwtMzA0NDE5
NTcwLDIwOTkwNDEzNDYsMTYzODAyMTE0NywxNzU4MzQzNjk3LC
0yMDgzMjAwMDEzLC0xNDE2NTMzMTMzLDY1NTg1MDUxNSwxMDQy
OTM3NTI1LDE3MjM3MDQxMDEsMjU5OTcwMzQ2LC0xODAwMTczMD
k2LDY1NTg1MDUxNSwtNTMxNDAxNTgxLC0yNDU4NTkwNSwtMTMy
NzMxMzEyMl19
-->