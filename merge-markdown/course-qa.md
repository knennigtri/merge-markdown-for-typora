# Use merge-markdown in QA mode
**Prerequisite:** merge-markdown must be [installed](install.md)

## Update manifest to use QA

manifest.md:

```yaml
qa: {exclude: "(frontmatter|preamble)"}
```

The line above will exclude any files that contain `frontmatter` or `preamble` in the filename. Any exclusion regex is accepted.



## Run in QA mode

1. Run merge-markdown

   1. Open a terminal to your project and run the command

   ``` bash
   merge-markdown -m yourManifest.md --qa
   ```

   2. The script above generates
      1. `fileName.qa.md`

## Advantages to QA Mode

Skips any specified content from the manifest-– frontmatter, preamble, copyright, etc…

Linkchecker

* All output creates a <filename>.linkcheck.md file
* Validates all assets and URLs in the file

TOC and bookmarks can be auto created. 

* 0 human interaction needed to create a single markdown file for PDF export.