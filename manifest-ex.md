---
input:
 frontmatter.md: ""
 path/to/module1.md: {noYAML: true, TOC: true}
 path/to/module2.md: {noYAML: true, TOC: true}
output: 
 name: output/MyContentGuide.md
qa: {exclude: "(frontmatter|preamble)"}
replace:
 <!--{timestamp}-->: 12/15/2021
 <!--{returnToMainTOC}-->: "[Return to Course Contents](#course-contents)"
 <!--{title}-->: My Enablement Title
 <!--{subtitle}-->: The guide to learning faster
 <!--{author}-->: Chuck Grant
 <!--{contactInfo}-->: merge@markdown.com
 <!--{creator}-->: My enablement organization
 <!--{subject}-->: New content creation techniques
 <!--{abstract}-->: Aenean sed leo lobortis, mollis sapien id, rutrum ante. Sed vitae pellentesque lorem. Donec dignissim venenatis dolor vulputate scelerisque. Curabitur dapibus mattis dolor, vel iaculis nulla tempus id.
---