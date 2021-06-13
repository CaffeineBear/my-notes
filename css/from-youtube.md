http://www.youtube.com/watch?v=1Rs2ND1ryYc

Linking css files
```html
<link rel="stylesheet" type="text/css"  href="some-directory">
```

Selectors and Properties

- Selectors
  - grabbing html
  - element selector `p`, `body` and etc.
  - id selector `#someid`
  - class selector `.someclass`

- specificity -> overwriting hierarchy in css
  - `inline html` > `id` > `class` > `element`

- should use class multiple times while only one time with id.


Pseudoselectors

- e.g. `h2:hover`
- selecting child -> `li:first-child`, `li:last-child` or `li:nth-child(n)` (note not the ul)
- `only-child` -> the one that has single child.
- `#id:link` for before clicking link `#id:visited` for after clicking link


Advanced Selectors

- One follow the other: e.g. `h2 + a` -> every anchor tag followed by h2.

- General sibling combinator:
  - One followed by other but they have to have same parents.
  - `textarea ~ button`

- Child Selector
  - `ul > li`
  - every li within ul.
  - li has to be direct child of ul.

- Descendant selector
  - `ul li`
  - Any li who has ul as ancestor.


Attribute Selectors
https://youtu.be/1Rs2ND1ryYc?t=3644


Coloring and Formatting



Fonts and Text Manipulations
