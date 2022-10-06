# Use merge-markdown for Review
**Prerequisite:** merge-markdown must be [installed](install.md)

Depending on the review type, you can either output the module file from [Typora as a PDF](https://support.typora.io/Export/#pdf) or you can have more control with [merge-markdown](https://github.com/knennigtri/merge-markdown/blob/main/README.md#supported-output-options).

Consider:

```
+ My Course
  + myModule1
  + myModule2
    + links
    - myModuleFile.md
    - moreInformation.md
```


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
 path/to/myModuleFile.md: {noYAML: true, doctoc: true}
 path/to/moreInformation.md: {noYAML: true}
output: 
 name: myAwesomeModule.md
replace:
 <!--{timestamp}-->: 05/30/2021
 <!--{returnToMainTOC}-->: "[...back to main TOC](#course-contents)"
```

