---
input:
 frontmatter.md: ""
 m1/m1-example.md: {noYAML: true, TOC: true, replace: {<!--#-->: "Module 1:"}}
 m2/m2-example.md: {noYAML: true, TOC: true, replace: {<!--#-->: "Module 2:"}}
output: 1-md-output/enablementGuide.md
qa: {exclude: "(frontmatter)"}
replace:
 <!--{timestamp}-->: 12/15/2021
 <!--{returnToMainTOC}-->: "[Return to Course Contents](#course-contents)"
 <!--{title}-->: My Enablement Title
 <!--{subtitle}-->: The guide to learning faster
 <!--{author}-->: Chuck Grant
 <!--{contactInfo}-->: myemail@email.com
 <!--{creator}-->: My enablement organization
 <!--{subject}-->: New content creation techniques
 <!--{abstract}-->: Aenean sed leo lobortis, mollis sapien id, rutrum ante. Sed vitae pellentesque lorem. Donec dignissim venenatis dolor vulputate scelerisque. Curabitur dapibus mattis dolor, vel iaculis nulla tempus id.
---