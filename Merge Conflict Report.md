# Text Merge Details
Date: 10/26/2019, 11:41:06 PM

```json
[Browser Info]
{
  "appVersion": "5.0 (Macintosh)",
  "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:69.0) Gecko/20100101 Firefox/69.0",
  "platform": "MacIntel"
}
```

Document: [Active Issues](/app#id=4dbcPjup6LFV86L3)

Client Length: 202

Server Length: 1643

Merge Length: 1790

Client Hash: 1779652259

Server Hash: 1942188576

Merge Hash: 299428618

# Content


|Client|Server|Merge|
|-|-|-|
|# Active Issues<br />* Data corruption when merging data between 3+ clients.<br /><br />## Workspaces<br />* Grav<br />* StackEditPro<br />## Publish<br />* Blogger<br />* Dropbox<br />* GitHub<br />* GitLab<br />* Google Drive<br />* Wordpress<br />* Zendesk<br />* Grav<br />|# Data Corruption<br />There is an ongoing data corruption when merging data between 3+ clients.  The core sync engine incorrectly senses that files need to be merged, and odd remnants appear. <br /><br />When a merge happens, we add a *Merge Conflict Report* document to your workspace to indicate what was merged and when it happened.  You can then view the history of your document if you need to fix it.  The merge report also includes the pre and post merge versions for your convenience.<br /><br />In our experience, most situations that require a merge really needed the server version.  An the default merge operation resulted in a corrupt document.  We decided that when it is detected that the servand client changed, we will keep the server, and create a report with all 3 versions (client, server, and merge).<br /><br /># Move File Dialog<br />The window in not tall enough.  It should size to full screen.  Use a filtered choice picker.<br /><br /># iOS Resize<br />The application does not respond to orientation changes well.<br /><br /># Source Code Documentation Extension<br />~~Parameter descriptions are not implemented for Typescript interface methods.~~<br /><br /># Zendesk Publishing Not Implemented<br />Send us an email if you require Zendesk support.<br /><br /># Sharing<br />The sharing server does not render mermaid, fences, or other canvas-based extensions.<br /><br /># Feature Requests<br />* Add scrolling divs (or toolbar popup) to toolbar.  Tools are not available on a narrow device.<br />* Export canvas as png.<br />* Create plugin architecture.<br />* Tasks<br />	* Complete task from task report.<br />	* Integrate tasks with external systems.<br />	* Scroll to line when selecting search and task links.<br />* Document driven design integration.<br /><br />|# Data Corruption<br />There is an ongoing dActive Issues<br />* Data corruption when merging data between 3+ clients.  The core sync engine incorrectly senses that files need to be merged, and odd remnants appear. <br /><br />When a merge happens, we add a *Merge Conflict Report* document to your workspace to indicate what was merged and when it happened.  You can then view the history of your document if you need to fix it.  The merge report also includes the pre and post merge versions for your convenience.<br /><br />In our experience, most situations that require a merge really needed the server version.  An the default merge operation resulted in a corrupt document.  We decided that when it is detected that the servand client changed, we will keep the server, and create a report with all 3 versions (client, server, and merge).<br /><br /># Move File Dialog<br />The window in not tall enough.  It should size to full screen.  Use a filtered choice picker.<br /><br /># iOS Resize<br />The application does not respond to orientation changes well.<br /><br /># Source Code Documentation Extension<br />~~Parameter descriptions are not implemented for Typescript interface methods.~~<br /><br /># Zendesk Publishing Not Implemented<br />Send us an email if you require Zendesk support.<br /><br /># Sharing<br />The sharing server does not render mermaid, fences, or other canvas-based extensions.<br /><br /># Feature Requests<br />* Add scrolling divs (or toolbar popup) to toolbar.  Tools are not available on a narrow device.<br />* Export canvas as png.<br />* Create plugin architecture.<br />* Tasks<br />	* Complete task from task report.<br />	* Integrate tasks with external systems.<br />	* Scroll to line when selecting search and task links.<br />* Document driven design integration.<br /><br /><br />## Workspaces<br />* Grav<br />* StackEditPro<br />## Publish<br />* Blogger<br />* Dropbox<br />* GitHub<br />* GitLab<br />* Google Drive<br />* Wordpress<br />* Zendesk<br />* Grav<br />|

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTcxNDE3MzM4M119
-->