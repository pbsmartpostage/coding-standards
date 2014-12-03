# CSS Style Guide

## Spacing

* Use soft-tabs with a four (4) space indent. Spaces are the only way to guarantee code renders the same in any person's environment.
* Put spaces after : in property declarations.
* Put spaces before { in rule declarations.
* Put line breaks between rulesets.
* When grouping selectors, keep individual selectors to a single line.
* Place closing braces of declaration blocks on a new line.
* Each declaration should appear on its own line for more accurate error reporting.

## Formatting

* Use hex color codes #000 unless using rgba().
* Use // for comment blocks (instead of /* */).
* Avoid specifying units for zero values, e.g., margin: 0; instead of margin: 0px;.
* Strive to limit use of shorthand declarations to instances where you must explicitly set all the available values.
* List related properties together

## Selectors

* Use hyphens in selectors. Do not use camel case, or underscores.

```css
// bad
.myClass {
...
}

// bad
.my_class {
...
}

// good
.my-class {
...
}
```

## Specificity

**Never** use ids as selectors. If you must use an id selector (please don't) make sure that you have no more than one in your rule declaration. A rule like #header .search #quicksearch { ... } is considered harmful.

* Good (not really) candidates for ids: header, footer, modal popups.
* Bad candidates for ids: navigation, item listings, item view pages (ex: issue view).