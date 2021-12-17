# Modular Markdown for a single PDF

The goal of this project is to be able to write markdown in a modular format while still being able to create a single PDF for output. This process allows for you to have many different module/chapter files and then combine them into a seamless PDF with table of contents and PDF bookmarks. The 3 primary tools that are needed are:

* [Typora](https://typora.io/) editor
  * Other editors can be used though this guide is written with Typora in mind.
* The [merge-markdown](https://www.npmjs.com/package/merge-markdown) tool (npm module)
* *Optional*: Adobe Acrobat (automated professional PDF output)

Common types content that could benefit from modular workflow:

* technical manuals
* training manuals
* documentation
* tutorials
* college courses

New to markdown? Take a look at the simple syntax: https://www.markdownguide.org/basic-syntax/

## Merge-Markdown advantages

Using the merge markdown tool offers several advantages:

* Modularize your content (multiple files) into chapters, sections, exercises/topics, references, etc.
* Files are then build into a single markdown file based on the manifest file
* All markdown files go through a link checker ensuring all links are valid (assets and expternal URLs)
* The manifest file provides:
  * ability to add a TOC per file
  * Add find/replace variables per file
  * removal of YAML per file
  * Add metadata to the PDF
  * Global find/replace variables
  * name the output markdown file

## Typora advantages

Although any markdown editor could be used. Typora adds serveral unique advantages for simple markdown editing:

* Available for all platforms
* [OOTB themes](https://theme.typora.io/) - themes are customizable as well
* [WYSIWYG editor](https://medium.com/@martineder/typora-markdown-as-wysiwyg-as-it-can-get-3cad302c0566) that shows realtime themes
* [Export markdown](https://support.typora.io/Export/) to different formats such as PDF, html, pandoc, word, OpenOffice, and more..
* Ability to add [header/footers](https://support.typora.io/Export/#header--footer) onto an output
* [YAML frontmatter](https://support.typora.io/YAML/). Write typora specific configurations into YAML at the top of your markdown to be read for output, image location, etc..

## Useful Tips

#### Development suggestions

1. Use the the [module-starter.md](module-starter.md) to start writing
   1. For best modularization, you should keep assets in a seperate folder per markdown file. See [Suggested Markdown Project Setup](#suggested-markdown-project-setup)
2. Follow the [quickguide-rules.md](quickguide-rules.md) to keep consistent formatting
3. Develop a standard project structure such as the [Suggested Markdown Project Setup](#suggested-markdown-project-setup)

#### Suggested Markdown Project Setup

Creating a well organized project structure helps keep things organized and easy to reference in the long run. Realistically the [merge-markdown](https://www.npmjs.com/package/merge-markdown) tool can handle any project structure as long as the manifest references the files propertly.

source (folder)

* frontmatter.md
* module-one
  * links (folder)
  * module-one.md
* module-x
  * links (folder)
  * module-x.md
* manifest.md

## Suggested Typora configuration

Although Typora is not needed, the biggest advantage I suggest using typora is the ability to auto create a [table of contents](https://support.typora.io/Markdown-Reference/#table-of-contents-toc) for an entire document and translate that into PDF bookmarks on export. It's as simple as adding `[TOC]` into your frontmatter.md file to have it auto-generated for the final PDF.

Other editors have the ability to create TOCs but typora is by far the easiest to work with.

### PDF CSS add-on Theme

In [typora-pdf-add-on-theme](typora-pdf-add-on-theme) folder there is a add-on theme that gives a few quality of life css rules for better PDF output for a modular/chapter type of PDF.

### Suggested Configurations

In the menu go to `Typora  > Preferences`

Under the Appearance Tab

* Themes: **choose your desired default theme**
* Click **Open Theme Folder**
* Copy/paste all files and folders from [typora-pdf-add-on-theme](typora-pdf-add-on-theme) into the **Theme Folder**

Under the **Image** Tab

- When Insert: **Copy Image to custom folder** = `./links/${filename}`
- Make to **select**
  - [x] Apply above rules to local images
  - [x] Apply above rules to online images
  - [x] Use relative path if possible

Under the **Markdown** tab **select**

- [x] **Display line numbers for code fences**
- [x] **Auto wrap long lines**

Under the **Export** tab
- Click PDF template and update these values
  - Paper Size: **US Letter**
  - Margin: **Custom**
    - **19mm** for all margins
  - Theme: **choose your desired theme**
  - [x] Read and overwrite export settings from YAML front matters
  - [x] Open exported file

**Restart Typora to have all settings applied**
