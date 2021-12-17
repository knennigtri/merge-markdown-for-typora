# Use merge-markdown for Review

Depending on the review type, you can either output the module file from Typora as a PDF or you can have more control with merge-markdown.

Consider:

```
+ My Course
  + myModule1
  + myModule2
    + links
    - myModuleFile.md
    - moreInformation.md
```

### Prework

1. Have [Typora](https://typora.io/) installed

2. Install npm: https://www.npmjs.com/get-npm

3. Install merge-markdown:

   ``` bash
   $ npm install -g merge-markdown
   ```

> Learn more about this project here: https://www.npmjs.com/package/merge-markdown



## Basic module output

```bash
merge-markdown -m myModule2
```

This will output a single file called `myModule2.out.md` that can then be exported from typora into PDF format



## Controlled module output

Just like you can create a course manifest, you can create a module manifest to better control the generatede output:

Add `myModule2-manifest.md` to `myModule2` folder:

```yaml
input:
 path/to/myModuleFile.md: {noYAML: true, TOC: true}
 path/to/moreInformation.md: {noYAML: true}
output: myAwesomeModule.md
replace:
 <!--{timestamp}-->: 05/30/2021
 <!--{returnToMainTOC}-->: "[...back to main TOC](#course-contents)"
```

