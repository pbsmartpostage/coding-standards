# HTML Style Guide

## Spacing / Formatting

* Use soft-tabs with a four (4) space indent. Spaces are the only way to guarantee code renders the same in any person's environment.
* Use good spacing between sections.
* Use double quotes (") on attribute values.

```html
<div class="my-class">
    <div class="sub-class"></div>
</div>

<div class="my-class">
    <div class="sub-class"></div>
</div>
```

## IDs / Class Names

Use hyphens in ids and class names. Do not use camel case, or underscores.

```html
// bad
<div id="myID"></div>

// bad
<div class="my_class"></div>


// good
<div id="my-id" class="my-class"></div>
```

