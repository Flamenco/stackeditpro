# Source-Code-Documentation Extension

Document source code outside of your codebase and render it as beautiful HTML.

# Usage

To trigger the *Source Code Documentation Extension*, do one of the following:
* Create a `yml` code fence having the first line an string item named `sig:`.
* Create a `ts` code fence having the first item a comment of `//@doc`.

# Examples
## Single Method Documentation
```yml
sig: "repeatString(text: string, times: number): string[]"
desc: Repeats a string the specified number of times.
params:
 text: The string you want to repeat.
 times: How many times to repeat.
ret: The string concatenated the requested number of times
```

```yml

sig: "repeatString(text: string, times: number): string[]"
desc: Repeats a string the specified number of times.
params:
 text: The string you want to repeat.
 times: How many times to repeat.
ret: The string concatenated the requested number of times
```

> If the `sig` has colons with trailing spaces, make sure to use quotes around the value to conform with the 	`YAML` specification.  Alternatively , you can also use a multline string such as `sig: |` or `sig: >`.

We use `Typescript` notation to define the method signature.

## Interface Documentation
You can also generate documentation from a Typescript interface by including the special comment `//@doc` as the first line of the code fence.  Any single line comments preceding declared items will become descriptions.

```ts
//@doc
// This is an interface comment
interface Foo {
  // This is a property comment.
  myProperty: string
  // This is a function comment.
  myFunction(myParam:string[]): string 
}
```

```ts

//@doc
// This is an interface comment
interface Foo {
  // This is a property comment.
  myProperty: string
  // This is a function comment.
  myFunction(myParam:string[]): string
}
```

# Description Styles
You can add descriptions to your Typescript interfaces by using comments.

There are 4 comment styles supported:  `single`, `consecutive`, `inline`, and `multiline`.

You do not need to use JavaDoc `/** ... **/` notation.
```ts
//@doc
interface CommentStyles extends Styles {
// Single line comment
a: string
// Consecutive
// line
// comment
b: string
c: string // Inline comment
/*
 Multiline
 comment
*/
d: string
}
```

# Themes
There are currently 2 themes, light (the default) and dark.

To enable the dark theme, add the `theme-dark` class to any parent element.
# Other Features (Pending)
The documentation can be displayed in a variety of ways by using templates and/or custom CSS.

The documentation can be pushed into or extracted from the source code.

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTkxOTkwMTM4MSw1MDEyNTQyMTUsLTEwND
EyNTA3MTYsLTEyMjg3Mzk4ODcsMTQ3NDA1NzQxNCwtMTg1Mjg3
OTczMyw4OTg4NTYzMTAsLTExNjc5Njc5NDQsLTEwNTkyODg0Nz
NdfQ==
-->