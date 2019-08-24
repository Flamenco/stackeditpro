Import and export *Grav* websites to and from any workspace folder.

# Grav Website Structure
Grav websites have a directory for each web page.  The directories name is the page name, and it contains a markdown file for the page content.  Thas file uses a name that determines the content template used for rendering the page.  The page content may also contain a *Frontmatter Header*.  Pages can contain nested pages.

```text
- https://www.foo.com
	- Page 1
		- default
	- Page 2
		- default
		- Page 3
			- default
		- Page 4
			- default
```

> The  StackEditPro `Page Title Extension` will use the folder title when displaying the page preview.

# Usage

## Configure Grav Site
You will need to install and configure our *StackEditPro Connector* on your Grav site.  The connector is available from Grav's Plugin Repository.
* Install `Grav CORS plugin`
	* Enable `GET` and `POST`.
* Install the `StackEditPro Connector plugin`.
* Set your access key in the `StackEditPro Connector` settings.
* Add `header("Access-Control-Allow-Headers: content-type");` to  your Grav installations `index.php`.  There is no Grav plugin (like the CORS plugin) available for this.

## Download Your Grav Site To StackEditPro Workspace
* Select the `Get Grav` action.
* Enter your site URL.
* You Grav website will be downloaded to a top level folder with the site's host name.

## Make Changes In Your Workspace
You can add new folders, subfolders, and template files.  If you need to delete a file or folder, you must do that on the Grav site directly.

## View A Difference Report
The report show what has been added, removed, and modified.

## Push Your Changes
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIxNDM5NDI4NDEsMTMxNDAwMDc0N119
-->