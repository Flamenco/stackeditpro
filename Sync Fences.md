# Syntax

You create a Sync Fence by including code between lines of `@@@`, similar to code fences that use backticks.

The first lines of a sync fence, up to the first blank line, are used to configure fields.
Each field is a name, 1 or more `=` or ` `  characters, and then the value.

|Field| Type |Description |
|--|--|--|
| id | [a-zA-Z0-9]+ | The ID of the sync fence to declare. |
|ref| [a-zA-Z0-9]+ | The ID of the sync fence to reference. |
|link| true \| false | Link the reference to the source. |

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
eyJoaXN0b3J5IjpbLTE4MTM5MjYxMzFdfQ==
-->