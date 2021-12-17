# PDF CSS Add-on

Typora provides basic PDF output. This CSS add-on adds enhanced TOC rules, logical breaks points after certain headers tags, and helpful typora hints to understand what the PDF output will look like.

## General Provided css rules

All of these rules are avaiable in the typora UI because of the [typora-ui.css](pdf-css-addon/typora-ui.css) file.

* Table of Contents

  * `h1`, `h2`, and `h3` will show in the TOC

  * `h4`, `h5`, and `h6` do not show in the TOC
* Page Break: before

  * `h1` (except first h1), `h2`
* Page Break: after

  * `[TOC]`
* Page Break: none

  * first `h1` take of file
  * `h3`, `h4`, `h5`, `h6`
* Page Break: avoid
  * Code blocks
  * blockquotes
  * tables
  * lists
  * Paragraphs

* Manual page break
  * Include `<div class="page-break"></div>` in your markdown file. See [page breaks](https://support.typora.io/Page-Breaks/)


## Add addon theme to Typora

This theme is considered add on because it's added using the [base.user.css file](https://support.typora.io/Add-Custom-CSS/) that allows these css rules to be added to any selected theme.

To add this add-on theme:

1. Open Typora. From the menu select **Preferences**
2. Under **Appearance** click on **Open Themes folder** at the bottom
3. Copy these files into the Themes folder:
   1. base.user.css
   2. pdf-css-addon (folder)
4. Restart Typora



