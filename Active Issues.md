# Data Corruption
There is an ongoing data corruption when merging data between 3+ clients and a server.  The core sync engine incorrectly senses that files need to be merged, and odd remnants appear in the merged result. 

When a conflict occurs, we now add a *Merge Conflict Report* document to your workspace to indicate what would have been merged and when it happened.  You can then view the history of your document if you need to fix it.  The merge report also includes the pre and post merge versions for your convenience.

In our experience, most situations that require a merge really needed the server version.  An the default merge operation resulted in a corrupt document.  **We decided that when it is detected that the server and client changed, we will keep the server, and create a report with all 3 versions (client, server, and merge)**.

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
~~* Add scrolling divs (or toolbar popup) to toolbar.  Tools are not available on a narrow device.~~
* Export canvas as png.
* Create plugin architecture.
* Tasks
	* Complete task from task report.
	* Integrate tasks with external systems.
	* Scroll to line when selecting search and task links.
* Document driven design integration.

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4NDMxNTQ5MTYsMzIwMTA0NjEsMzk4OT
U0OTA5LDE4NDkyNjYwODIsMTU0MzM4NTQ5OSwtMTU5MDMzNDA5
OSwxNTQzMzg1NDk5LC05NDcxMTA4MjIsLTMwNDQxOTU3MCwyMD
k5MDQxMzQ2LDE2MzgwMjExNDcsMTc1ODM0MzY5NywtMjA4MzIw
MDAxMywtMTQxNjUzMzEzMyw2NTU4NTA1MTUsMTA0MjkzNzUyNS
wxNzIzNzA0MTAxLDI1OTk3MDM0NiwtMTgwMDE3MzA5Niw2NTU4
NTA1MTVdfQ==
-->