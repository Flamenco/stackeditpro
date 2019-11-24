# Overview
A *Sync Fence* is a block of markdown that can be reused among multiple documents.  When a *SyncFence* is modified,, all references will update.  You simply wrap code in a *Sync Fence*, and then reuse it in other documents.  This keeps your source DRY.

This is very useful for page summaries, notices, and footers.
```
[Document 1]
 @@@ fence1
 Hello, *World*!
 @@@
```

```
[Document 2]
 Here is the fence:

 @@@ fence1 @@@
```

*Sync Fences* are ideal for defining page level text, such as footers. In general, they keep your content *DRY*.

# Syntax

The syntax is simple.  Declare a fence using a line starting with `@@@ someId` and ending with `@@@`.
Then reference it using `@@@someID@@@`.

You create a Sync Fence by including code between lines of `@@@`, similar to code fences that use backticks.

The first lines of a sync fence, up to the first blank line, are used to configure fields.
Each field is a name, 1 or more `=` or ` `  characters, and then the value.

|Field| Type |Description |
|--|--|--|
| id | [a-zA-Z0-9]+ | The ID of the sync fence to declare. |
|ref| [a-zA-Z0-9]+ | The ID of the sync fence to reference. |
|link| true \| false | Link the reference to the source. |

## Alternate Notation
You can specify configuration fields using the following syntax.  KeyValue pairs followed by a blank line.
You must specify one of `id` or `ref`, and this must be first.
```
@@@
id=someid
showRefs=true

Your content here
@@@

@@@
ref=someid
link=true
@@@
```

# Styles
You can add CSS styles to rendered source and reference fences.  The `syncfence-error` style is used for invalid syntax and unresolved references.
```css
syncfence-src {
  color: green;
}
syncfence-ref {
  color: red;
}
syncfence-error {
  color: orange;
}
.syncfence-link {
  color: green;
}


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExNDc4NjE3NjAsMTkzMTMzNTc0OCwxMj
cxNjU0MzBdfQ==
-->