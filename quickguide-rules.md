### Markdown Rules

Most of these rules can be modified to your preference, unless specified. Along with the title rules below, markdown syntax should be used. See [quickguide-markdown.md](quickguide-markdown.md). Anything in parenthesis () is based on the [typora-pdf-addon-theme](typora-pdf-addon-theme)

* Modules should be broken up into separate files for better modularity
* H1 - only used for title at the top of the file (inTOC=yes)
* H2 - Used for top level topics (inTOC=yes)
* H2 -  Exercises titles (inTOC=yes)
  * H4 is used for tasks/sub-exercises (inTOC=no)
* H3 - used for subtopics (inTOC=yes)
* H4 - used for sub-subtopics (inTOC=no)
* H5 - used for sub-sub-subtopics (inTOC=no)
* H6 - used for sub-sub-sub-subtopics (inTOC=no)

## General things to know

* You can optionally add a module (per file) TOC to help with navigation
  * Take a look at the `<!-- -->` content in  [module-starter.md](module-starter.md) 
* frontmatter.md can be consistered static and can dynmically change based on [find/replace variables](https://www.npmjs.com/package/merge-markdown#replace-keys-within-a-single-file) in the merge-markdown manifest. See example [manifest-ex.md](manifest-ex.md).
* References should be inline with a unique ID so you can have the actual links at the bottom of the file. This allows all references within a single file to be managed at the bottom of the file.
  * References should not be used in headings. Add the reference to a sentence or paragraph below.
  * **Inline** reference Syntax `[my Documentation][intro1]`
  * URL for refernce should be at the **bottom** with syntax: `[intro1]: www.myexample.com`
