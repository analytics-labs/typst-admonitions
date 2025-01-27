# Asciidoctor-like Admonitions for Typst

## Usage

Import this package:

```typ
#import "admonitions.typ": *
```

then use the predefined admonitions found in `admonitions.typ` or just import `lib.typ` and define your own admonition styles.

## Pre-defined admonitions

```typ
#tip[
  #lorem(10)
]
```

creates a simple admonition of type `tip`.

## Example Admonitions

![Example 1](page-1-of-4.png)

![Example 2](page-2-of-4.png)

![Example 3](page-3-of-4.png)

![Example 4](page-4-of-4.png)

## Define your own admonitions

*Definition*

```typ
#let myadmonition(
  type: "My Admonition",
  title: none,
  bar: gray,
  icon: emoji.llama,
  
  body
) = admonition(
  type: type,
  title: title,
  bar: bar,
  icon: icon,
  
  body)
```

*Usage*

```typ
#myadmonition[
  #lorem(20)
]

#myadmonition(title: [_Hello, World!])[
  #lorem(20)
]
```

![Example 5](myadmonition1.png)

```typ
#let mycoloredadmonition(
  type: "My Admonition",
  title: none,
  bar: gray,
  icon: emoji.llama,
  background-color: green.lighten(40%),
  radius: 1em,
  border: green,
  
  body
) = admonition(
  type: type,
  title: title,
  bar: bar,
  icon: icon,
  background-color: background-color,
  radius: radius,
  border: border,
  
  body)

#mycoloredadmonition[
  #lorem(20)
]

#mycoloredadmonition(title: [_Hello, World!_])[
  #lorem(20)
]
```

![Example 6](myadmonition2.png)