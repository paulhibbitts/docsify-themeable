# Customization

## Theme Styles

To customize a *docsify-themeable* [theme](themes):

1. Add a `<style>` tag after the theme stylesheet in your `index.html`:

   ```html
   <!-- Theme -->
   <link rel="stylesheet" href="https://unpkg.com/docsify-themeable/dist/css/theme-simple.css">

   <!-- Custom theme styles -->
   <style>
     /* ... */
   </style>
   ```

   If you prefer, you can use a `<link>` to an external stylesheet:

   ```html
   <!-- Theme -->
   <link rel="stylesheet" href="https://unpkg.com/docsify-themeable/dist/css/theme-simple.css">

   <!-- Custom theme stylesheet -->
   <link rel="stylesheet" href="theme-custom.css">
   ```

1. Set any of the [theme properties](#theme) found below:

   ```css
   :root {
     --base-font-size: 14px;
     --theme-color   : purple;
   }
   ```

   ?> It's easy to to mix styles from different themes! Just [view the source of other themes](https://github.com/jhildenbiddle/docsify-themeable/tree/master/src/scss/themes), find the theme properties you like, and copy them to your custom stylesheet.

### Base

Theme properties for base styles.

[_base.css](https://raw.githubusercontent.com/jhildenbiddle/docsify-themeable/master/src/scss/themes/defaults/_base.css ':include :type:code')

### Content

Theme properties for markdown content.

[_content.css](https://raw.githubusercontent.com/jhildenbiddle/docsify-themeable/master/src/scss/themes/defaults/_content.css ':include :type:code')

### Cover

Theme properties for docsify's [`coverpage`](https://docsify.js.org/#/cover).

[_cover.css](https://raw.githubusercontent.com/jhildenbiddle/docsify-themeable/master/src/scss/themes/defaults/_cover.css ':include :type:code')

### Misc

Theme properties for miscellaneous elements.

[_misc.css](https://raw.githubusercontent.com/jhildenbiddle/docsify-themeable/master/src/scss/themes/defaults/_misc.css ':include :type:code')

### Navbar

Theme properties for docsify's custom [`navbar`](https://docsify.js.org/#/custom-navbar).

[_navbar.css](https://raw.githubusercontent.com/jhildenbiddle/docsify-themeable/master/src/scss/themes/defaults/_navbar.css ':include :type:code')

### Sidebar

Theme properties for docsify's custom [`sidebar`](https://docsify.js.org/#/more-pages).

[_sidebar.css](https://raw.githubusercontent.com/jhildenbiddle/docsify-themeable/master/src/scss/themes/defaults/_sidebar.css ':include :type:code')

## Plugin Styles

All [docsify plugins](https://docsify.js.org/#/plugins) will work with *docsify-themeable*, however there are two potential issues to be aware of:

- **Not all plugins support multiple themes**

  Plugins often inject CSS to style plugin-related elements. Ideally, a plugin's CSS would inherit visual styles from the current theme. This isn't always practical, so some plugins will apply visual styles intended to match a specific theme (typically the default `vue.css` theme). The result is color, typography, and layout styles that do not match your site theme.

- **Not all plugins support theme customization**

  Many [docsify plugins](https://docsify.js.org/#/plugins) were developed prior to the release of *docsify-themeable* and therefore do not offer theme customization. To address this issue, *docsify-themeable* provides customizable theme properties for many popular docsify plugins (below). If you would like to see theme properties added to a plugin, create a [Github issue](https://github.com/jhildenbiddle/docsify-themeable/issues) with the plugin name and a link to the source code.

### Copy Code

Theme properties for [docsify-copy-code](https://github.com/jperasmus/docsify-copy-code) plugin.

[_plugin-copycode.css](https://raw.githubusercontent.com/jhildenbiddle/docsify-themeable/master/src/scss/themes/defaults/_plugin-copy-code.css ':include :type:code')

### Pagination

Theme properties for [docsify-pagination](https://github.com/imyelo/docsify-pagination) plugin.

[_plugin-pagination.css](https://raw.githubusercontent.com/jhildenbiddle/docsify-themeable/master/src/scss/themes/defaults/_plugin-pagination.css ':include :type:code')

### Search

Theme properties for docsify's [search](https://docsify.js.org/#/plugins?id=full-text-search) plugin.

[_plugin-search.css](https://raw.githubusercontent.com/jhildenbiddle/docsify-themeable/master/src/scss/themes/defaults/_plugin-search.css ':include :type:code')

### Zoom Image

Theme properties for docsify's [zoom image](https://docsify.js.org/#/plugins?id=zoom-image) plugin.

[_plugin-zoom.css](https://raw.githubusercontent.com/jhildenbiddle/docsify-themeable/master/src/scss/themes/defaults/_plugin-zoom-image.css ':include :type:code')

## PrismJS

[PrismJS](http://prismjs.com/) is the syntax highlighter used by [docsify](https://docsify.js.org/) for styling code blocks. Styles can be customized by setting [`--code`](#-code) theme properties or by using one of the many [PrismJS themes](https://unpkg.com/prismjs/themes/) available.

To use a PrismJS theme, add a `<link>` to your `index.html` after your site theme:

```html
<!-- Site theme -->
<link rel="stylesheet" href="https://unpkg.com/docsify-themeable/dist/css/theme-defaults.min.css">

<!-- PrismJS theme -->
<link rel="stylesheet" href="path/to/prismjs-theme.css">
```

Note that only PrismJS theme colors will be applied. Layout and typography styles such as `font-family`, `border-radius`, `margin` and `padding` will continue to be applied by the site theme to maintain visual consistency.

The [theme properties](#theme) that override PrismJS theme values are:

- `--code-font-family`
- `--code-font-size`
- `--code-font-weight`
- `--code-block-border-radius`
- `--code-block-line-height`
- `--code-block-margin`
- `--code-block-padding`