Import and synchronize *Grav* websites to and from any workspace folder.

# Overview
You can import any number of Grav websites into your StackEditPro workspace.
Each imported site will then sync to each of your workspace devices;
You can download the site on one device and then edit it from any other device synced to that workspace.

When you are done editing, push some are all of your changes back to Grav from any device.

If you modify your content directly on Grav, you will need to delete the folder on StackEditPro and re-download it.

# Grav Website Structure
Grav websites have a directory for each web page.  The directory name is the folder or page name; It contains a markdown file containing the page content.  The markdown file's name determines the *content template* used for rendering the page, and *not the page title*.

The page content may also contain a *Frontmatter Header*.

Pages can contain nested pages.

```text
- https://www.foo.com
	- Page 1
		- default
	- Page 2
		- fancy
		- Page 3
			- default
		- Page 4
			- fancy
```

> The  StackEditPro `Page Title Extension` will use the folder title,  not the template name, when displaying a page preview.

# Usage

## Configure Grav Site
You will need to install and configure our *StackEditPro Connector* on your Grav site.  The connector is available from Grav's Plugin Repository.
* Install the `StackEditPro Connector plugin`.
	* Set an access key in the `StackEditPro Connector` settings.
* Configure the `Grav CORS plugin` (This is installed as a dependency when installing the StackEditPro Connector plugin).
	* Enable *allow-method* for at least `GET` and `POST`.
	* Enable *allow-header* for at least `content-type`and `x-stackeditpro-api-key`.
	* Enable *Manage Preflight Requests*.

## Download Your Grav Site To StackEditPro Workspace
* Select the `Get Grav...` action.
* Enter your site URLs.  You must prefix each URL with your access key: `secret@https://mysite.com`
* Your Grav website will be downloaded to a *top level folder* with the folder name set to your Grav site's host name.

## Make Changes In Your Workspace
You can add new folders, subfolders, and markdown template files to StackEditPro, but you must follow Grav's naming convention.  If you need to delete, move, or rename a file or folder, it must be done on the Grav site directly.

## View A Difference Report
The report show what has been added, removed, and modified.

## Push Your Changes
Only new and modified files and directories on the StackEditPro workspace will be updated on the Grav server.  This is a one-way sync that modifies, but never removes server data.

# Issues
* For security reasons, Grav sites must support valid https.  You may run into browser issues if connecting to an http site from the the StackEditPro https site.

# TODO
* Allow deleting, renaming, and moving pages from StackEditPro.
* Show server-only files.
* Add refactoring features.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjY5MzQ5ODQwLC0yMTQzNjIzOTUwLDE4MT
UwNTkxMSwtODc3MzM5MzAxLC00MTIwMjEwOTEsMTA0NDMyNzU5
NSwtMTI4MDM1OTgxMywxNjc4Njg0Nzg4LC0xOTU4MDg4MzE0LC
0xODcwNzUxNzQwLC0xMzU5NzkyNDIyLDEzNzIzMzI5MDgsMTky
MzA0NTU2NCw1MjgyNjM0NzcsLTE3ODIyMDQwMTQsLTMxNjcyNT
U4MiwxMDk0NjI3Mjc4LDUyMzE0MTQ0NywyNjY2MTQwOTYsMzM4
ODk4NzA0XX0=
-->