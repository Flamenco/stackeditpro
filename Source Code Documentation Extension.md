# Source-Code-Documentation Extension

Document source code outside of your codebase and render it as beautiful HTML.

# Usage

To trigger the *Source Code Documentation Extension*, do one of the following:
* Create a `yml` code fence having the first line an string item named `sig:`.
* Create a `ts` code fence having the first item a comment of `//@doc`.

# Examples
## Method or Property Documentation (using YAML)
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

You can also use an 	`array` instead of `object` for `params`.  This will apply the descriptions in order of declaration, allow you to omit the parameter name.

```yml

sig: "repeatString(text: string, times: number): string[]"
desc: Repeats a string the specified number of times.
params:
 - The string you want to repeat.
 - How many times to repeat.
ret: The string concatenated the requested number of times
```

> If the `sig` has colons with trailing spaces, make sure to use quotes around the value to conform with the 	`YAML` specification.  Alternatively , you can also use a multiline string such as `sig: |` or `sig: >`.

> We use `Typescript` notation to define the method signature.

## Interface Documentation
You can also generate documentation from a Typescript interface by including the special comment `//@doc` as the first line of the code fence.

Comments preceding declared items will become descriptions.

```ts
//@doc
// This is an interface comment
interface Foo {
  // This is a property comment.
  myProperty: string
  // This is a function comment.
  myFunction(
  myParam:string[] // A parameter comment.
  ): string 
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
Several comment styles are supported:  `single`, `consecutive`, `inline`, and `multiline`.

The comment engine will add periods to the end of your rendered descriptions if they do not already exist.

> You **do not** need to use JavaDoc `/** ... **/` notation.
```ts
//@doc
interface CommentStyles extends Styles {
  // A single line comment
  singleLine: string
  // A consecutive
  // line
  // comment
  consecutiveLine: string
  inline: string // An inline comment
  /*
   A multiline
   comment
  */
  multiLine: string
}
```

# Themes
There are currently 2 themes, *light* (the default) and *dark*.

To enable the *dark theme*, add the `theme-dark` class to any parent element.
# Other Features (Pending)
The documentation can be displayed in a variety of ways by using templates and/or custom CSS.

The documentation can be pushed into or extracted from the source code.

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2NDIyODY2MDUsMTA0MDQ1OTU1MywxOD
IyNzQxODc0LC0yMTQxNzU5NDAsLTE5OTE5NTU3NTIsMTA5OTQ0
MzkwLDEzMDk1NTE4MiwyMzc5NjQ5NTEsLTkxOTkwMTM4MSw1MD
EyNTQyMTUsLTEwNDEyNTA3MTYsLTEyMjg3Mzk4ODcsMTQ3NDA1
NzQxNCwtMTg1Mjg3OTczMyw4OTg4NTYzMTAsLTExNjc5Njc5ND
QsLTEwNTkyODg0NzNdfQ==
-->