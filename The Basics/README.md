# The Basics of CSS

1. The Basics

    a) Specificity

    b) Rules of CSS

    c) Cascade & Inheritance

    d) Box Model Basics


## CSS Specificity 

The means by which a browser decides which CSS property values are the most relevant & need to be applied. This can be calculated by `selector types`. 

CSS reads from top to bottom, so these selectors will introduce specificity to a stylesheet, introducing style priorities.

### Ranking Selector Types 

0. Inline styles added to an element (i.e. `style="font-weight: bold"`) always overwrite any styles in external stylesheets
1. Type selectors (i.e. `h1`) and pseudo-elements (i.e. `::before`)
2. Class selectors (i.e. `.example`), attributes selectors (i.e. `[type="radio"]`) and pseudo-classes (i.e. `:hover`)
3. ID selectors (i.e. `#example`)

Universal selector (`*`), combinators (`+`, `>`, `~`) and negation pseudo-class (`:not()`) have no effect on specificity. 

### The `!important` Exception

Using `!important` to override any other declaration is bad practice and should be avoided because it makes debugging difficult by disrupting the natural cascading in stylesheets. 

### The `:not` Exception

The negation pseudo-class of `:not` is _not_ considered a pseudo-class in the specificity calculation.