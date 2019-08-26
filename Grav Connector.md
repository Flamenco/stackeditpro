Import and synchronize *Grav* websites to and from any workspace folder.

# Overview
You can import any number of Grav websites into your Grav workspace.
Each imported site will sync to all of your workspace devices;
You can download the site on one device and then edit it from any other device synced to that workspace.

When you are done editing, push your changes back to Grav from any device.

If you modify your content directly on Grav, you should delete the folder on StackEditPro and re-download it.

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
You can add new folders, subfolders, and template files to StackEditPro.  If you need to delete, move, or rename a file or folder, you must do that on the Grav site directly.

## View A Difference Report
The report show what has been added, removed, and modified.

## Push Your Changes
Only new and modified files and directories on the StackEditPro workspace will be updated on the Grav server.

# Issues
* Grav sites must support valid https.  
# TODO
* Allow deleting, renaming, and moving pages from StackEditPro.
* Show server-only files.
* Add refactoring features.
<!--stackedit_data:
eyJoaXN0b3J5IjpbNTI4MjYzNDc3LC0xNzgyMjA0MDE0LC0zMT
Y3MjU1ODIsMTA5NDYyNzI3OCw1MjMxNDE0NDcsMjY2NjE0MDk2
LDMzODg5ODcwNCwtNjE5NjQxOTA0LDY4MjAxMjQ2OCwtMjU5OD
YwNjczLC0xODQ1Mjc1OTg1LDgwMTkxNzY1OSwxODUzNjI0MTMs
LTE3OTE4NTMwNywtMTg1NTI1Mjk4NiwtMjE0Mzk0Mjg0MSwxMz
E0MDAwNzQ3XX0=
-->