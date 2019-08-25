Import and synchronize *Grav* websites to and from any workspace folder.

# Overview
You can import any number of Grav websites into your Grav workspace.
Each imported site will sync to all of your workspace devices;
You can download the site on one device and then edit it from any other device synced to that wordp.

# Grav Website Structure
Grav websites have a directory for each web page.  The directory name is the page name, and it contains a markdown file for the page content.  The markdown file filename determines the content template used for rendering the page, and not the page name.

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

> The  StackEditPro `Page Title Extension` will use the folder title,  not the template name, when displaying the page preview.

# Usage

## Configure Grav Site
You will need to install and configure our *StackEditPro Connector* on your Grav site.  The connector is available from Grav's Plugin Repository.
* Install `Grav CORS plugin`
	* Enable allow-method `GET` and `POST`.
	* Enable allow-header `content-type`
* Install the `StackEditPro Connector plugin`.
	* Set your access key in the `StackEditPro Connector` settings.
* ~~Add `header("Access-Control-Allow-Headers: content-type");` to  your Grav installations `index.php`.  There is no Grav plugin (like the CORS plugin) available for this.~~

## Download Your Grav Site To StackEditPro Workspace
* Select the `Get Grav` action.
* Enter your site URL.
* You Grav website will be downloaded to a top level folder with the site's host name.

## Make Changes In Your Workspace
You can add new folders, subfolders, and template files.  If you need to delete a file or folder, you must do that on the Grav site directly.

## View A Difference Report
The report show what has been added, removed, and modified.

## Push Your Changes
Only new and modified files and directories on the StackEditPro workspace will be updated on the Grav server.

# TODO
* Allow deleting, renaming, and moving pages from StackEditPro.
* Add refactoring features.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMzI5NjY0MjkyLDEwOTQ2MjcyNzgsNTIzMT
QxNDQ3LDI2NjYxNDA5NiwzMzg4OTg3MDQsLTYxOTY0MTkwNCw2
ODIwMTI0NjgsLTI1OTg2MDY3MywtMTg0NTI3NTk4NSw4MDE5MT
c2NTksMTg1MzYyNDEzLC0xNzkxODUzMDcsLTE4NTUyNTI5ODYs
LTIxNDM5NDI4NDEsMTMxNDAwMDc0N119
-->