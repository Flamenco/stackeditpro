# Data Corruption
There is an ongoing data corruption when merging data between 3+ clients and a server.  The core sync engine incorrectly senses that files need to be merged, and odd remnants appear in the merged result. 

When a conflict occurs, we now add a *Merge Conflict Report* document to your workspace to indicate what would have been merged and when it happened.  You can then view the history of your document if you need to fix it.  The merge report also includes the pre and post merge versions for your convenience.

In our experience, most situations that require a merge really needed the server version.  And the default merge operation resulted in a corrupt document.  **We decided that when it is detected that the server and client changed, we will keep the server, and create a report with all 3 versions (client, server, and attempted merge)**.

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
* ~~ Add scrolling divs (or toolbar popup) to toolbar.  Tools are not available on a narrow device.~~
* Export canvas as png.
* Create plugin architecture.
* Tasks
	* Complete task from task report.
	* Integrate tasks with external systems.
	* Scroll to line when selecting search and task links.
* Document driven design integration.
* Open all external links in a new window.

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTI5Mzg0MjQxNSwxNTU4MzEzNTg3LC0xMT
ExMTczMjcxLDg4NTkzMDAxLC0zODE4NDkyMzYsMTQ1ODIwNzQx
NiwtMTg0MzE1NDkxNiwzMjAxMDQ2MSwzOTg5NTQ5MDksMTg0OT
I2NjA4MiwxNTQzMzg1NDk5LC0xNTkwMzM0MDk5LDE1NDMzODU0
OTksLTk0NzExMDgyMiwtMzA0NDE5NTcwLDIwOTkwNDEzNDYsMT
YzODAyMTE0NywxNzU4MzQzNjk3LC0yMDgzMjAwMDEzLC0xNDE2
NTMzMTMzXX0=
-->