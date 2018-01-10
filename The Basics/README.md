# The Basics of CSS

1. The Basics
    - [Specificity](##css-specificity)
    - [Rules of CSS]()
    - [Cascade & Inheritance]()
    - [Box Model Basics]()

## CSS Specificity 

Specificity is the set of rules that decides which style should dominate. This can be calculated by `selector types`. Each selector types' value ranges over a scale.
    
Specificity | Points | Example
----------- | ------ | -------
Most specific | 1000 pts. | inline styling
Moderately specific | 100 pts. | id
Less specific | 10 pts. | class, pseudo-class, attribute
Least specific | 1 pt. | elements

As CSS reads from top to bottom, these selectors will introduce a specific ranking to a stylesheet; style priorities.

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