[![Netlify Status](https://api.netlify.com/api/v1/badges/547e2215-6ab1-4a29-84f1-ef0d8fa8b508/deploy-status)](https://app.netlify.com/sites/upbeat-swirles-009f3e/deploys)

SPARC Infrastructure
====================

Jekyll-based site for SPARC’s data infrastructure reports & articles.

---

## Setting up 

Ruby is required.

1. `gem install jekyll`

## Running the site locally

1. `git clone https://github.com/sparcopen/infrastructure.git`
3. `cd infrastructure/`
4. `jekyll s`
5. Navigate to `http://127.0.0.1:4000` in your browser

## Building the site

1. `git clone https://github.com/sparcopen/infrastructure.git`
2. `cd infrastructure/`
3. `jekyll build`
4. Compiled static HTML, CSS, & JS will be found in `_site/`

---

## File structure

### Content 

All content can be found in:
- `_data/`: records for each author, in `authors.yml`
- `_posts`: individual posts in Markdown 
- `reports`: one Markdown file per report
- `topics`: one Markdown file per topic (_threads_)

### Stylesheets 

This project uses SASS (`.scss`) to organise all of the website’s stylesheets, found in [`_sass/`](https://github.com/sparcopen/infrastructure/tree/master/_sass). This directory is split into multiple directories containing partials (`.scss` files prefixed with `_`):

- `vendors`
  - Any third-party stylesheet; we only need a CSS reset to make sure the styles all look the same on various browsers (Normalize.css). If we were using third-party JS plugins with complex CSS, we might store it here, but rename it as a partial (`_[name of vendor].scss`).  
- `base`
  - Where we have our variables & mixins, that are re-used throughout the stylesheets. This is where we define things like colour palette, typeface sizes (`_typscale.scss`), classes for the grid (`_grid.scss`), and spacing (`_spacing.scss`). 
  - This approach helps us design a more uniform UI
- `components`
  - All basic and re-usable components are here: things like buttons, labels, infoboxes, tags... 
  - Component classes are based on BEM-style naming with the `block__element--modifier` naming convention. 
    - For example, we have the block `.button`, and the block & modifier `.button--cta` for buttons that are calls-to-action
    - Another example: the block `.infobox` can also have the element `.infobox__links` (elements can only be children of blocks; `.infobox__links` is never outside of `.infobox` in the HTML markup) 
- `layout`
  - Anything related to larger blocks of the UI: the layout. We have the page content (anything in the center / main area of the page), page footer & page-sidebar.
- `pages`
  - For page-specific styling: Homepage, Thread, Post, and About. 
  - We try to avoid having overly-specific styles and instead rely on re-usable components to design the UI.
- `themes`
  - Only contains print CSS styles: stylesheets for a different context. 

These files are then compiled (in that order) into a single static CSS file using imports in [`css/main.scss`](https://github.com/sparcopen/infrastructure/blob/master/css/main.scss). 

#### More about the pre-processor SCSS / SASS

SCSS files acccept plain CSS; it allows us to extend the language with features like variables and mixins. This also helps with reducing redundant code & improving uniformity. 

See the [SASS Basics](https://sass-lang.com/guide) guide.

We have a very basic use of SASS in our codebase:  
- variables: prefixed with `$`, as in `$red` or `$spacing-02`
- mixins: to include multiple CSS declarations, as in `@mixin font-monospace {...}`
  - we include a mixin with with `@include font-monospace`
- nesting: useful in components
  - try to avoid nesting more than three times, otherwise the CSS becomes too specific 
  - it is used in combination with the ampersand for BEM elements & modifiers, as with [`.infobox__links`](https://github.com/sparcopen/infrastructure/blob/master/_sass/components/_infobox.scss#L18)
 
#### Spacing system

In `_sass/base/_spacing.scss`, we define six spaces: `$spacing-01..$spacing-06`. These spaces are relative to the base font-size (`rem` units), which is 22px on large devices and 18px on smaller devices. 

Every time we declare `padding` or `margin`, we use a spacing variable. 

Spacing sizes start from smaller (`0.1875rem` = 3.75px on large devices) to larger (`12rem` = 240px on large devices):

#### Typescale system 

In `_sass/base/_typescale.scss`, we define six typeface sizes: `$typescale-01..$typescale-06`. This typescale is based on a [minor third interval](https://en.wikipedia.org/wiki/Minor_third). 

The typescale number (`-01..-06`) reflects heading size (from larger to smaller); see [the `_general.scss` stylesheet](https://github.com/sparcopen/infrastructure/blob/master/_sass/base/_general.scss). 

Every time we declare `font-size`, we use a typescale variable **or** `1em` to make sure the text is the same size as its parent element’s text. 



