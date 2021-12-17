# Single PDF Export

### Prework

1. Have [Typora](https://typora.io/) and Acrobat installed

2. Install npm: https://www.npmjs.com/get-npm

3. Install merge-markdown:

   ``` bash
   $ npm install -g merge-markdown
   ```

> Learn more about this project here: https://www.npmjs.com/package/merge-markdown

### Setup Single PDF output

1. Create the manifest file (ex: [manifest-ex.md](manifest-ex.md))

   1. `input:`

      1. `frontmatter.md` should be first
      2. the rest of the modules/files should follow expected PDF order
   
   2. `output:` is the location and name of final md output

   3. `replace:` The replace options below are required to make sure the frontmatter is properly created

      ```yaml
      <!--{timestamp}-->: 12/15/2021
      <!--{returnToMainTOC}-->: "[...back to main TOC](#course-contents)"
      <!--{courseTitle}-->: My Enablement Title
      <!--{author}-->: Chuck Grant
      ```
   
2. Run merge-markdown

   1. Open a terminal to your project and run the command

   ``` bash
   merge-markdown -m yourManifest.md
   ```
   2. The script above generates
      1. `yourOutputGuide.md` - Single output of all the specified input files based on the configuration rules set in the manifest. This is a good time to verify that the guide has been built properly
      2. `yourOutputGuide.linkcheck.md` - This is a quick QA to make sure there are no broken links within the final source document. This checks URLs as well as local asset files

3. In Typora, Verify the merged md file

   1. Validate the replaced variables
   2. Check global TOC
   3. Check module TOCs
   4. Verify references were built correctly
   5. Do a quick verification that assets are showing up correctly in typora
   7. Fix any issues, and perform the previous steps again.
   
4. Export the raw PDF

   1. Verify the PDF output (similar to previous step)

### Finalize the PDF

1. Make sure all QA checks have passed before continuing
2. Rename the PDF to the final title
3. (optional) Run the Adobe Acrobat [action](../acrobat) for a professional output
