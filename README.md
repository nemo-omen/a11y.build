# a11y.build

This is the source for [a11y.build](https://a11y.build), a site dedicated to teaching HTML, CSS, and JavaScript with accessibility as a fundamental part of the process.

This project is in the process of being built. At some point soon it will be ready to show the world.

## So what's a11y.build?
For now, the plan is to create the site as a series of lessons that teach the fundamentals of HTML, CSS, and JavaScript as though all of the most important accessibility features were necessary to make a site work properly because, when you think about it for a second, _they are necessary to make a site work properly_.

The site will be composed of two top-level pages: the blog, and the guide. The idea is to post new content to the blog as I learn it, then refine it and make it a part of the guide.

Eventually the guide will begin to solidify enough that it can be treated as a book or a course on fundamental, a11y-centered development.

Following all of that I imagine I'll want to create a third section with accessible components and how to implement them.

## Why?

The CDC estimates that [26% of adults in the US have some type of disability](https://www.cdc.gov/ncbddd/disabilityandhealth/infographic-disability-impacts-all.html). While there's a moral imperative to provide access to the content we create, there's also a professional imperative — we should strive to create sites that work as close to 100 percent of the time as possible. If we're creating sites that don't work well for 26% of people, we're creating sites that only work 74% of the time.

And nobody likes skating by with a C average, right?


## Astro & Accessible Astro Starter
This site is being created with [Astro](https://astro.build) and the [Accessible Astro Starter](https://github.com/markteekman/accessible-astro-starter) by [Mark Teekman](https://github.com/markteekman).

The original `readme.md` has been left intact below. 
## Accessible Astro Starter

This starter project is build upon the (awesome) [Astro Static Site Builder](https://astro.build/). This starter offers a couple of Accessibility components and some utility classes to get you building your project faster. Also check out the [Accessible Astro Components](https://github.com/markteekman/accessible-astro-components) npm package which can be used with (or without) this starter!

[Live demo](https://accessible-astro.markteekman.nl/)

### Installation
```console
npm init astro -- --template markteekman/accessible-astro-starter
```

### Accessibility features

In this starter you'll find a couple of things:

- Accessible landmarks in the `DefaultLayout.astro` file such as `header`, `main` and `footer`
- Accessible landmark examples in the `index.astro` file such as `section` and `nav`
- `SkipLinks.astro` component to skip to either the main menu or the main content
- `Navigation.astro` component with keyboard accessible navigation (arrow keys, escape key)
- `ResponsiveToggle.astro` component with an accessible responsive toggle button for the navigation
- `DarkMode.astro` component toggle with accessible button and a user system preferred color scheme
- Outline focus indicator which works on dark and light backgrounds
- `.sr-only` token class for screen reader only text content

### Other features

This starter contains some extra Design System like utility classes to aid in the global layout of your project. All of this can be found in the `public/scss/base` directory, and compiles in the `globals.scss` file. Using these primitives is totally optional, use or remove at your own preference :) What it contains:

- Reset file to reset browser defaults and ensure everything looks good
- Some basic font settings, such as responsive heading sizes
- Color shades for your color pallet, rendered to the `:root` of your website as custom properties
- Simple auto-grid setting using `display: grid` and a `data-attribute`
- A bit more advanced grid settings using `display` grid to easily setup a 12-column layout
- Utilities set in `_utility.scss` for things such as spacing, sizes, colors, and box-shadows

#### Using Auto Grid

Simply apply the `data-auto-grid` attribute on your parent `div` with a number from 2-6 (if you need more columns just tweak the for loop in `_auto-grid.scss`). The grid automatically creates new rows (this is how `display: grid` works by default).

```html
<div class="container" data-auto-grid="3">
  <p>First column</p>
  <p>Second column</p>
  <p>Third column</p>
</div>
```

You can also center the contents of the cell using the `data-grid-center` attribute. Use it together with `data-auto-grid`.

```html
<div class="container" data-auto-grid="3" data-grid-center>
  <!-- ... -->
</div>
```

_Examples are included in the index.astro file_

#### Using Grid

Grid enables you to build a little more complex layouts if need be. Using `display: flex;` you can define the amount of columns `.cells` should take up in your `.grid`, and for which breakpoint they should do so. You can also use offset on a grid to create an extra column of offset. For all examples check [my documentation website](https://markteekman.nl/project/flexbox-grid).

```html
<div class="container">
  <div class="grid gutters">
    <div class="cell small-12 medium-3">
      <h3>Sidebar</h3>
      <!-- ... -->
    </div>
    <div class="cell small-12 medium-8 offset-medium-1">
      <h3>Main</h3>
      <!-- ... -->
    </div>
  </div>
</div>
```

_Examples are included in the index.astro file_

#### Using Margin and Padding

To prevent spacing each element in your website individually and to prevent inconsistencies, you can use the `.margin-#` and `.padding-#` utility classes. A good practice is to set in on your `<section>` elements, for starters. To space out content you can use a special `.space-content` class on your parent div (for example in a `.cell` of your `.grid`). By default, margin/padding top and bottom are set with these utilities. You can also set it explicitly using either `.top` of `.bottom` class tokens. Find or tweak all spacing options in `_space.scss`.

```html
<section class="padding-32">
  <div class="container">
    <h2 class="margin-16 bottom">Grid example</h2>
  </div>
</section>
```

_Examples are included in the index.astro file_

#### Using Sizes

If you need an exception on your font-size for a specific reason you can use size utility classes to accomplish that. Using it is easy. Find or tweak all spacing options in `_size.scss`.

```html
<div class="container">
  <p class="size-20">I'm a bigger font size!</p>
</div>
```

_Examples are included in the index.astro file_

### Using Colors

You can setup your own color schemes in the `_colors.scss` file. You'll find a SCSS map, which gets printed inside `_root.scss` as custom properties.

```scss
$colors: (
  primary-clr: (
    100: hsl(262, 90%, 95%),
    200: hsl(262, 100%, 88%),
    300: hsl(262, 100%, 78%),
    400: hsl(268, 82%, 60%),
    500: hsl(273, 79%, 48%),
  ),
  // ...
);
```

### Helping out

If you find that something isn't working right then I'm also happy to hear it to improve this starter! Let me know by either:

1. [Filing an issue](https://github.com/markteekman/accessible-astro-starter/issues)
2. Or sending a [pull request](https://github.com/markteekman/accessible-astro-starter/pulls)

### Thank you!

A big thank you to the creators of this awesome Astro static site builder and to all using this starter to make the web a bit more accessible for all people around the world :)

[![buymeacoffee-button](https://user-images.githubusercontent.com/3909046/150683481-be070424-7bb0-4dd7-a3cb-43b5605163f5.png)](https://www.buymeacoffee.com/markteekman)
