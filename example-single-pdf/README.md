# Single Guide Example

Learn how to create a single PDF with these markdown files:  [course-release.md](../merge-markdown/course-release.md) 

To create a single PDF for the entire course there is 1 file needed:

* `manifest.md` - contains yaml configurations specifying the merge

frontmatter.md - Static file that is controlled by replace variables in the manifest

m1-example.md

- Styling based on [module-starter.md](../module-starter.md) 
- Create as many .md modules as needed

`src/1-md-output` - folder containing combined markdown files with [merge-markdown tool](../merge-markdown)

`src/2-raw-pdf-output` - folder containing raw PDF export

`src/3-final-pdf-output` - folder containing final PDFs
