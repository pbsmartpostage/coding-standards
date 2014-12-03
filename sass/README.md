# Sass Style Guide

## Follow the CSS Guidelines

Make sure you follow all of the [css guidelines](../css/), as they provide a good base for our SASS guidelines.

## List @extend(s) First

```scss
.weather {
  @extends %module; 
  ...
}
```

## List "Regular' Styles Next

```scss
.weather {
  @extends %module; 
  background: LightCyan;
  ..
}
```

## List @include(s) Next

```scss
.weather {
  @extends %module; 
  background: LightCyan;
  @include transition(all 0.3s ease-out);
  ...
}
```

## Nested Selectors Last

```scss
.weather {
  @extends %module; 
  background: LightCyan;
  @include transition(all 0.3s ease);
  > h3 {
    border-bottom: 1px solid white;
    @include transform(rotate(90deg));
  }
}
```

## Maximum Nesting: Three (3) Levels Deep

```scss
.weather {
  .cities {
    li {
      // no more!
    }
  }
}
```

## Be Generous With Comments

```scss
.overlay {
  // modals are 6000, saving messages are 5500, header is 2000
  z-index: 5000; 
}
```

## No Styles in the Main Sass

Keep styles out of the main compiled sass file(s). Only include other componentized sass files and settings, etc...

## Modularize!

Keep styles that belong together in separate files.

In general, our directory structure looks like this:

```
assets
├── base
│   ├── comments.scss
│   └── _typography.scss
├── components
│   ├── _button.scss
│   └── _dialog.scss
├── settings
│   ├── mixins
│   │   └── _button.scss
│   ├── variables
│   │   ├── _button.scss
│   │   ├── _colors.scss
│   │   └── _typography.scss
│   └── _settings.scss
└── app.scss
```

Good example of app.scss:

``scss
// Application
// ========================================

// Settings
// ========================================
@import "settings/settings";

// Base
// ========================================
@import "base/typography";

// Components
// ========================================
@import "components/button";
@import "components/dialog";
```

Our main settings file should also not contain any styles. It should just include settings broken down into multiple files. Here is an example of _settings.scss:

```scss
// Settings
// ========================================

// Variables
// ========================================
@import "variables/colors";
@import "variables/typography";
@import "variables/button";

// Mixins
// ========================================
@import "mixins/button";
```


