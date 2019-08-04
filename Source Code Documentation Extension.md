# Source-Code-Documentation Extension

Document source code outside of your codebase and render it as beautiful HTML.

# Usage

To trigger the *Source Code Documentation Extension*, do one of the following:
* Create a `yml` code fence having the first line an string item named `sig:`.
* Create a `ts` code fence having the first item a comment of `//@doc`.

# Examples
## Method or Property Documentation (using YAML)

You can include the following keys: `sig`, `desc`, `params`, and `ret`.

Use `Typescript` notation to define the method or property signature.  

```yml
 
sig: "repeatString(text: string, times: number): string[]"
desc: Repeats a string the specified number of times.
params:
 text: The string you want to repeat.
 times: How many times to repeat.
ret: The string concatenated the requested number of times
```

You can also use an 	`array` instead of `object` for `params`.  This will apply the descriptions in order of declaration, allowing you to omit the parameter name.

```yml

sig: "repeatString(text: string, times: number): string[]"
desc: Repeats a string the specified number of times.
params:
 - The string you want to repeat.
 - How many times to repeat.
ret: The string concatenated the requested number of times
```

> If the `sig` has colons with trailing spaces, make sure to use quotes around the value to conform with the 	`YAML` specification.  Alternatively, you can also use a multiline string such as `sig: |` or `sig: >`.

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
  myFunction(myParam:string[]): string
}
```

# Descriptions
You can add descriptions to your Typescript interfaces by using comments.
Several comment styles are supported, including  `single`, `consecutive`, `inline`, and `multiline`.

The comment engine will add periods to the end of your rendered descriptions if they do not already exist.

> You **do not** need to use JavaDoc `/** ... **/` notation.

```ts
 //@doc
interface CommentStyles extends Styles {
  // A single line comment
  singleline: string
  // A consecutive
  // line
  // comment
  consecutiveline: string
  inline: string // An inline comment
  /*
   A multiline
   comment
  */
  multiline: string
}
```

# Themes
There are currently 2 themes implemented, *light* (the default) and *dark*.

To enable the *dark theme*, add the `theme-dark` class to any parent element of the code fence.

# Other Features (Pending)
The documentation can be displayed in a variety of ways by using templates and/or custom CSS.

The documentation can be pushed into or extracted from the source code.

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4ODc0MTgxMjksLTEwMzQ2Mzg2MjUsLT
E4ODc0MTgxMjksMjYxNTY4MzI2LDU3MzQ1OTg4OCwtNzM1Mjk1
NTI4LDE2NDM5MTI5MjgsMTE2MjA5NzE3OCwtMTY0MjI4NjYwNS
wxMDQwNDU5NTUzLDE4MjI3NDE4NzQsLTIxNDE3NTk0MCwtMTk5
MTk1NTc1MiwxMDk5NDQzOTAsMTMwOTU1MTgyLDIzNzk2NDk1MS
wtOTE5OTAxMzgxLDUwMTI1NDIxNSwtMTA0MTI1MDcxNiwtMTIy
ODczOTg4N119
-->